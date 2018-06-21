# UiKitValidator

## Features:

*   validate mail input;
*   validate password input;
*   validate text input;
*   validate username input;

## Installation:

1. First You need to install uikit all instruction and files You have [here.](https://getuikit.com/) 
2. Download uikitValidator.js 
3. Link it in header ()

## How to use:

1. Under your form paste:
```
<script type="text/javascript">
  var validator = new My_Validator; 
  var submitButton = document.getElementById("yourSubmitButtonId");
  var form = document.getElementById("yourFormId");
</script> 
```
2. Now You have to get all Your inputs like that:
```
var usernameInput = document.getElementById("yourUsernameInputId");
```
You can have other like: 
```
var passInput = document.getElementById("yourPasswordInputId");
```
3. Then You have to create var formInputs array, and keep here all your inputs:
```
var formInputs = [usernameInput, passInput];
```
4. And now u have to add listeners to every input and submit button 
```
//example 
usernameInput.addEventListener("keyup", function() { validator.validate(usernameInput,submitButton,"type"); }); 
```
**Instead "type" use: **
**- "password", **
**- "username", **
**- "text", **
**- "mail"**<br/>
And for submit button use this:
```
submitButton.addEventListener("click",function(event){ validator.submit(submitButton,formInputs,event); });
```
