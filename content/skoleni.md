---
draft: false
title: 📑 Školení
params:
  hidemeta: true
  showtoc: false
  ShowBreadCrumbs: false
---

<style type="text/css">
    .itemlist {
        list-style-type: none;
    }
    .itemlist li {
        margin-top:0.7em;
    }
    .red {
        color: red;
        margin-left: 0.3em;
    }

    .err {
        color: red;
        visibility: hidden;
    }

    #successDiv {
        background-color: #d4edda;
        color:black;
        padding: 1em;
        border-radius: 1em;
        float:none;
        clear:both;
        margin-top:1em;
        display: none;        
    
    }

    #errorDiv {
        background-color: #f8d7da;
        color:black;
        padding: 1em;
        border-radius: 1em;
        float:none;
        clear:both;
        margin-top:1em;
        display: none;        
    }

    #sendMessageForm {
        max-width: 500px;
        margin:0 auto;
        background-color: #2F2F2F;
        padding: 1.3em;
        border-radius: 1em;
    }

    #sendMessageForm label {
        display: block;
        font-weight: bold;
        font-size: 12pt;
    }

    #sendMessageForm input,
    #sendMessageForm textarea {
        background-color: white;
        padding: 0.5em;
        border-radius: 5px;
        width: 100%;
        margin-top: 0.3em;
    }

    #sendMessageForm button {
        background-color: white;
        color: black;
        padding-left: 1em;
        padding-right: 1em;
        padding-top: 0.5em;
        padding-bottom: 0.5em;
        border-radius: 0.3em;
        float: right;
        margin-top: 1em;
    }
</style>

<script src="https://www.google.com/recaptcha/api.js?render=6LeK1mkqAAAAAFy3v2kXD0TSBHdUkDUdEpatn907"></script>
<script type="text/javascript">

    window.onload = function(){


        var name = document.getElementById('formName');
        var email = document.getElementById('formEmail');
        var phone = document.getElementById('formPhone');
        var nameErr = document.getElementById("nameErr");
        var emailErr = document.getElementById("emailErr");
        var phoneErr = document.getElementById("phoneErr");
    
        //hide validation message on input
        name.addEventListener("keydown", function () {
            nameErr.style.visibility = "hidden";
        });
        email.addEventListener("keydown", function () {
            emailErr.style.visibility = "hidden";
        });
        phone.addEventListener("keydown", function () {
            phoneErr.style.visibility = "hidden";
        });
    
    
    
        function validateForm() {
    
            var name = document.getElementById('formName');
            var email = document.getElementById('formEmail');
            var phone = document.getElementById('formPhone');
            var nameErr = document.getElementById("nameErr");
            var emailErr = document.getElementById("emailErr");
            var phoneErr = document.getElementById("phoneErr");
    
            var isValid = true;
    
    
            if (!name.value) {
                nameErr.style.visibility = "visible";
                isValid = false;
            } else {
                nameErr.style.visibility = "hidden";
            }
    
            if (!email.value) {
                emailErr.style.visibility = "visible";
                isValid = false;
            } else {
                emailErr.style.visibility = "hidden";
            }
    
            if (!phone.value) {
                phoneErr.style.visibility = "visible";
                isValid = false;
            } else {
                phoneErr.style.visibility = "hidden";
            }
    
            return isValid;
        }
    
        window.onFormClick = function () {
    
            let serverHost = "https://mrthompsonapp.azurewebsites.net";

            if (!validateForm()) {
                return;
            }
    
            grecaptcha.ready(function () {
                grecaptcha.execute('6LeK1mkqAAAAAFy3v2kXD0TSBHdUkDUdEpatn907', { action: 'submit' }).then(function (token) {
                    //send post request from form including the recaptcha token to mrthompsonapp.azurewebsites.net
                    var form = document.getElementById("sendMessageForm");
                    var formData = new FormData(form);
                    formData.append("g-recaptcha-response", token);
    
                    fetch(serverHost + "/api/SendMessage", {
                        method: "POST",
                        body: formData
                    }).then(function (response) {
                        if (response.ok) {
                            var success = document.getElementById("successDiv");
                            success.style.display = "block";
                        } else {
                            var error = document.getElementById("errorDiv");
                            error.style.display = "block";
                        }
                    });
                });
            });
        }


    }
    
</script>
<div style="margin:0">
    <div class="col2">
        <img src="/ich.jpg" width="200" alt="Miroslav Thompson" />
    </div>
    <div class="col1">
        Nabízím školení a konzultace v oblasti softwarové architektury, softwarového inženýrství, cloudu, DevOps a kontejnerové orchestrace.
        <br /><br />
        Mám zkušenosti s výukou v následujících oblastech:
        <br /><br />
        <ul class="itemlist">
            <li><img src="https://upload.wikimedia.org/wikipedia/commons/f/fa/Microsoft_Azure.svg" width="25" style="display:inline;margin:0;"/> <strong>Azure</strong></li>
            <li>💻 <strong>Azure Devops</strong> - organizace, pipelines, skriptování</li>
            <li>👷 <strong>IT architektura</strong>: on-prem, cloud, hybrid, migrace, rozpočty, monitoring, bezpečnost, SaaS/PaaS/IaaS, atd.</li>
            <li>👷‍♂️ <strong>Softwarové inženýrství</strong> - životní cyklus projektu, architektura aplikace, programování a DevOps</li>
            <li><img src="https://upload.wikimedia.org/wikipedia/commons/3/39/Kubernetes_logo_without_workmark.svg" width="25" style="display:inline;margin:0;"/> <strong>Kubernetes</strong></li>
            <li>📱 <strong>Programování mobilních aplikací</strong></li>
        </ul>
    </div>
</div>


<h2 style="text-align: center;margin-top:1em;">Mám zájem o školení</h2>

<form id="sendMessageForm">
    <div class="form-input">
        <label for="name">Jméno<span class="red">*</span></label>
        <input id="formName" type="text" name="name">
        <span id="nameErr" class="err">Vyplňte prosím své jméno</span>
    </div>
    <div class="form-input">
        <label for="name">Email<span class="red">*</span></label>
        <input id="formEmail" type="email" name="email">
        <span id="emailErr" class="err">Vyplňte prosím validní email</span>
    </div>
    <div class="form-input">
        <label for="name">Telefon<span class="red">*</span></label>
        <input id="formPhone" type="phone" name="phone">
        <span id="phoneErr" class="err">Vyplňte prosím svůj telefon</span>
    </div>
    <div class="form-input">
        <label for="name">Zpráva</label>
        <textarea id="formMessage" name="message">
        </textarea>
    </div>
    <button type="button" onclick="window.onFormClick()">Odeslat</button>
    <br style="float:none;clear:both;" />
    <div id="successDiv">
        ✅ Zpráva byla odeslána, děkuji. Jakmile to bude možné, ozvu se Vám.
    </div>
    <div id="errorDiv">
        ❌ Něco se pokazilo. Zkuste to prosím znovu.
    </div>

</form>