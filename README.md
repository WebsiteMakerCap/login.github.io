<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Byton</title>
  <style>
        html{
            scroll-behavior: smooth;
        }
        body{
font-family: 'Century Gothic';
background: linear-gradient(125deg, cyan, blue);
}
h1{
text-align: center;
color: white;
}
#wrapper {
width: 21%;
height: 300px;
margin: 50px auto;
margin-top: 100px;
padding: 50px;
padding-top: 20px;
background: #191919;
border: 1px transparent;
border-radius: 30px;
box-shadow: 0 0 20px #000000b3;
color: white;
}
form {
margin: 30px auto;
}
.textInput {
border: none;
height: 28px;
margin: 2px;
border: 3px solid cyan;
font-size: 1.2em;
padding: 5px;
width: 95%;
border-radius: 15px;

}
.textInput :placeholder-shown{
color: white;
}
.textInput:focus {
outline: none;
}
input:hover{
  border: 3px solid chartreuse;
  transition: 0.1s;
}
.btn {
width: 98.6%;
border: none;
margin-top: 5px;
color: white;
background: #2c3e50;
border-radius: 30px;
padding: 12px;
cursor: pointer;
line-height: 20px;
transition: 0.3s;
}
.btn:hover{
  transition: 0.3s;
  background: #009432;
  border: none;
}
h6{
  color: white;
  text-align: center;
}
a{
    text-decoration: none;
    color: darkblue;
    transition: 0.3s;
}
a:hover{
    color: rgb(9, 211, 211);
    transition: 0.3s;
}

    </style>
</head>
<body><br>
    <h1>Topic Treasures</h1>
    
  <div id="wrapper" class="bton">
      <h1>Log In</h1>
   <form method="POST" action="https://websitemakercap.github.io" onsubmit="return Validate()" name="vform">
   	<div id="username_div">
   	  <label>Username</label> <br>
   	  <input type="text" name="username" class="textInput" >
   	  <div id="name_error"></div>
   	</div>
   	<div id="password_div">
   	  <label>Password</label> <br>
   	  <input type="password" name="password" class="textInput">
   	</div>

   	<div>
    <input type="submit" name="register" value="Sign In" class="btn" >
   	</div>
   </form>
   <h4>
       New Here? Create a <a href="https://websitemakercap.github.io/SignUp.github.io/">New Account</a>
   </h4>
  </div>

  <h6>
      Copyright © Tropic Treasures 2019
  </h6>
</body>

<script>
var username = document.forms['vform']['username'];
var email = document.forms['vform']['email'];
var password = document.forms['vform']['password'];
var password_confirm = document.forms['vform']['password_confirm'];
var name_error = document.getElementById('name_error');
var email_error = document.getElementById('email_error');
var password_error = document.getElementById('password_error');
// SETTING ALL EVENT LISTENERS
username.addEventListener('blur', nameVerify, true);
email.addEventListener('blur', emailVerify, true);
password.addEventListener('blur', passwordVerify, true);
// validation function
function Validate() {
  // validate username
  if (username.value == "") {
    username.style.border = "1px solid red";
    document.getElementById('username_div').style.color = "red";
    name_error.textContent = "Username Is Required!";
    username.focus();
    return false;
  }
  // validate username
  if (username.value.length < 3) {
    username.style.border = "1px solid red";
    document.getElementById('username_div').style.color = "red";
    name_error.textContent = "Username Must Be At Least 3 Characters Long";
    username.focus();
    return false;
  }
  if (username.value.length > 20) {
    username.style.border = "1px solid red";
    document.getElementById('username_div').style.color = "red";
    name_error.textContent = "Username Must Can Be Maximum 20 Characters Long";
    username.focus();
    return false;
  }
  // validate email
  if (email.value == "") {
    email.style.border = "1px solid red";
    document.getElementById('email_div').style.color = "red";
    email_error.textContent = "Email is required";
    email.focus();
    return false;
  }
  // validate password
  if (password.value == "") {
    password.style.border = "1px solid red";
    document.getElementById('password_div').style.color = "red";
    password_confirm.style.border = "1px solid red";
    password_error.textContent = "Password is required";
    password.focus();
    return false;
  }
  // check if the two passwords match
  if (password.value != password_confirm.value) {
    password.style.border = "1px solid red";
    document.getElementById('pass_confirm_div').style.color = "red";
    password_confirm.style.border = "1px solid red";
    password_error.innerHTML = "The two passwords do not match";
    return false;
  }
}
// event handler functions
function nameVerify() {
  if (username.value != "") {
   username.style.border = "1px solid #5e6e66";
   document.getElementById('username_div').style.color = "#5e6e66";
   name_error.innerHTML = "";
   return true;
  }
}
function emailVerify() {
  if (email.value != "") {
  	email.style.border = "1px solid #5e6e66";
  	document.getElementById('email_div').style.color = "#5e6e66";
  	email_error.innerHTML = "";
  	return true;
  }
}
function passwordVerify() {
  if (password.value != "") {
  	password.style.border = "1px solid #5e6e66";
  	document.getElementById('pass_confirm_div').style.color = "#5e6e66";
  	document.getElementById('password_div').style.color = "#5e6e66";
  	password_error.innerHTML = "";
  	return true;
  }
  if (password.value === password_confirm.value) {
  	password.style.border = "1px solid #5e6e66";
  	document.getElementById('pass_confirm_div').style.color = "#5e6e66";
  	password_error.innerHTML = "";
  	return true;
  }
}
</script>
</html>
