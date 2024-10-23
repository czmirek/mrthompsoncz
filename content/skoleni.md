---
draft: false
title: 📑 Školení
params:
  hidemeta: true
  showtoc: false
  ShowBreadCrumbs: false
---

Nabízím školení.

<style type="text/css">
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

    #sendMessageForm {
        max-width: 500px;
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
    
            if (!validateForm()) {
                return;
            }
    
            grecaptcha.ready(function () {
                grecaptcha.execute('6LeK1mkqAAAAAFy3v2kXD0TSBHdUkDUdEpatn907', { action: 'submit' }).then(function (token) {
                    //send post request from form including the recaptcha token to mrthompsonapp.azurewebsites.net
                    var form = document.getElementById("sendMessageForm");
                    var formData = new FormData(form);
                    formData.append("g-recaptcha-response", token);
    
                    fetch("https://mrthompsonapp.azurewebsites.net/api/SendMessage", {
                        method: "POST",
                        body: formData
                    }).then(function (response) {
                        if (response.ok) {
                            var success = document.getElementById("successDiv");
                            success.style.display = "block";
                        } else {
                            console.log("Něco se pokazilo. Zkuste to prosím znovu.");
                        }
                    });
                });
            });
        }


    }
    
</script>

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
</form>