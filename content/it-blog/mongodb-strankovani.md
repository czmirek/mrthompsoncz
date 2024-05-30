+++
title = 'MongoDB stránkování pro C#'
date = 2021-11-23T15:45:47+02:00
draft = false
+++

Následující kód jsem [od někud](https://kevsoft.net/2020/01/27/paging-data-in-mongodb-with-csharp.html) ukradl a trochu modifikoval. Jedná se o extension metodu, kterou lze zavolat nad `IMongoCollection<TDocument>` a vrátí to výsledek typu `ListResult<TDocument>` (jeho definice je níže) který obsahuje:

- data
- celkový počet dokumentů (`estimatedDocumentCount` má rychlost O(1))
- filtrovaný počet dokumentů
- počet stránek

Nepodařilo se mi ale zjistit, jak sloučit ten `estimatedDocumentCount` s tím agregovaným výstupem. V tuto chvíli tato extension metoda volá MongoDB 2x: nejdřív to vrátí agregovaný výstup skrz aggregate a pak se k tomu připojí ten `estimatedDocumentCount`. Líbilo by se mi, kdyby to bylo jen 1 volání ale nepřišel jsem na to, jak ten `estimatedDocumentCount` do toho aggregate výstupu dostat.

```csharp
public static async Task<ListResult<TDocument>> ListResultAsync<TDocument>(
        this IMongoCollection<TDocument> collection,
        int pageIndex = 0,
        int pageSize = 10,
        FilterDefinition<TDocument> filterDefinition = null,
        SortDefinition<TDocument> sortDefinition = null)
    {
        var countFacet = AggregateFacet.Create("count",
            PipelineDefinition<TDocument, AggregateCountResult>.Create(new[]
            {
                PipelineStageDefinitionBuilder.Count<TDocument>()
            }));
        var stages = new List<PipelineStageDefinition<TDocument, TDocument>>();
        if (sortDefinition != null)
            stages.Add(PipelineStageDefinitionBuilder.Sort(sortDefinition));
        stages.AddRange(new[]
        {
            PipelineStageDefinitionBuilder.Skip<TDocument>(pageIndex * pageSize),
            PipelineStageDefinitionBuilder.Limit<TDocument>(pageSize)
        });
        var dataFacet = AggregateFacet.Create("data", PipelineDefinition<TDocument, TDocument>.Create(stages));
        var aggregationQuery = collection.Aggregate();
        if (filterDefinition != null)
            aggregationQuery = aggregationQuery.Match(filterDefinition);
        var aggregation = await aggregationQuery.Facet(countFacet, dataFacet).ToListAsync();
        var count = aggregation.First()
            .Facets.First(x => x.Name == "count")
            .Output<AggregateCountResult>()
            .FirstOrDefault()
            .Count;
        var data = aggregation.First()
            .Facets.First(x => x.Name == "data")
            .Output<TDocument>();
        return new ListResult<TDocument>
        {
            Data = data,
            TotalRowsUnfiltered = await collection.EstimatedDocumentCountAsync(),
            TotalPagesFiltered = (int)Math.Ceiling((double)count / pageSize),
            TotalRowsFiltered = count
        };
    }

```

A zde je ten `ListResult<TDocument>`

```csharp
public class ListResult<T>
{
    public long TotalRowsUnfiltered { get; set; }
    public long TotalRowsFiltered { get; set; }
    public int TotalPagesFiltered { get; set; }
    public IEnumerable<T> Data { get; set; }
}
```