<!DOCTYPE html>
<html>
<head>
<title>La mia prima WebApp</title>
</head>

<body>

<h1>La mia prima WebApp 🚀</h1>

<p>Scrivi il tuo nome:</p>

<input id="nome">

<button onclick="saluta()">Invia</button>

<p id="risposta"></p>

<script>
function saluta() {
let nome = document.getElementById("nome").value;
document.getElementById("risposta").innerHTML = "Ciao " + nome + "!";
}
</script>

</body>
</html>
