<!DOCTYPE html>
<html>
<head>
<title>Gestione visite pazienti</title>

<style>
body{
font-family:Arial;
background:#f2f2f2;
text-align:center;
}

.container{
background:white;
padding:20px;
margin:30px auto;
width:350px;
border-radius:10px;
box-shadow:0 0 10px rgba(0,0,0,0.1);
}

input{
margin:5px;
padding:8px;
width:90%;
}

button{
padding:10px;
background:#2a7ae2;
color:white;
border:none;
border-radius:5px;
margin-top:10px;
}

table{
margin:auto;
margin-top:20px;
border-collapse:collapse;
}

td,th{
border:1px solid #ccc;
padding:8px;
}
</style>

</head>

<body>

<div class="container" id="login">

<h2>Login</h2>

<input id="user" placeholder="Username">
<input id="pass" type="password" placeholder="Password">

<button onclick="login()">Accedi</button>

<p id="errore"></p>

</div>


<div id="admin" style="display:none">

<h1>Admin - Gestione pazienti</h1>

<div class="container">

<h3>Aggiungi paziente</h3>

<input id="nome" placeholder="Nome paziente">
<input id="ospedale" placeholder="Ospedale">
<input id="reparto" placeholder="Reparto">
<input id="stanza" placeholder="Stanza">

<button onclick="aggiungi()">Salva paziente</button>

</div>

<h3>Pazienti presenti</h3>

<table id="tabella">

<tr>
<th>Nome</th>
<th>Ospedale</th>
<th>Reparto</th>
<th>Stanza</th>
</tr>

</table>

</div>

<script>

let utenti = [
{user:"admin",pass:"1234"}
]

function login(){

let u = document.getElementById("user").value
let p = document.getElementById("pass").value

if(u=="admin" && p=="1234"){
document.getElementById("login").style.display="none"
document.getElementById("admin").style.display="block"
}else{
document.getElementById("errore").innerHTML="Login non valido"
}

}

function aggiungi(){

let nome = document.getElementById("nome").value
let ospedale = document.getElementById("ospedale").value
let reparto = document.getElementById("reparto").value
let stanza = document.getElementById("stanza").value

let tabella = document.getElementById("tabella")

let riga = tabella.insertRow()

riga.in
