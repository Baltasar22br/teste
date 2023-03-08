# teste<!DOCTYPE html>
<html>
<head>
	<title>Teste de Procrastinação</title>
	<link rel="stylesheet" type="text/css" href="style.css">
</head>
<body>
	<h1>Teste de Procrastinação</h1>
	<form id="procrastinacao">
		<fieldset>
			<legend>Pergunta 1:</legend>
			<label><input type="radio" name="pergunta1" value="0"> Quase nunca</label><br>
			<label><input type="radio" name="pergunta1" value="1"> De vez em quando</label><br>
			<label><input type="radio" name="pergunta1" value="2"> Com frequência</label><br>
			<label><input type="radio" name="pergunta1" value="3"> Sempre</label>
		</fieldset>
		<fieldset>
			<legend>Pergunta 2:</legend>
			<label><input type="radio" name="pergunta2" value="0"> Quase nunca</label><br>
			<label><input type="radio" name="pergunta2" value="1"> De vez em quando</label><br>
			<label><input type="radio" name="pergunta2" value="2"> Com frequência</label><br>
			<label><input type="radio" name="pergunta2" value="3"> Sempre</label>
		</fieldset>
		<fieldset>
			<legend>Pergunta 3:</legend>
			<label><input type="radio" name="pergunta3" value="0"> Quase nunca</label><br>
			<label><input type="radio" name="pergunta3" value="1"> De vez em quando</label><br>
			<label><input type="radio" name="pergunta3" value="2"> Com frequência</label><br>
			<label><input type="radio" name="pergunta3" value="3"> Sempre</label>
		</fieldset>
		<fieldset>
			<legend>Pergunta 4:</legend>
			<label><input type="radio" name="pergunta4" value="0"> Quase nunca</label><br>
			<label><input type="radio" name="pergunta4" value="1"> De vez em quando</label><br>
			<label><input type="radio" name="pergunta4" value="2"> Com frequência</label><br>
			<label><input type="radio" name="pergunta4" value="3"> Sempre</label>
		</fieldset>
		<input type="button" value="Enviar" onclick="calcularResultado()">
	</form>
	<div id="resultado"></div>
	<script src="script.js"></script>
</body>
</html>
JavaScript:

css
Copy code
function calcularResultado() {
  var form = document.forms["procrastinacao"];
  var pontuacao = 0;

  for (var i = 0; i < form.elements.length; i++) {
    if (form.elements[i].type === "radio" && form.elements[i].checked) {
      pontuacao += parseInt(form.elements[i].value);
    }
  }

  var resultado = document.getElementById("resultado");
  resultado.innerHTML = "<p>Sua pontuação final é: " + pontuacao + "</p>";
}
