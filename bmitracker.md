<html>
<head>
<style>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
  overflow: auto;
  background-color: #333;
}

li {
  float: left;
}

li a {
  display: block;
  color: white;
  text-align: center;
  padding: 14px 16px;
  text-decoration: none;
}

li a:hover {
  background-color: #111;
}
</style>
</head>
<body>
<ul>
  <li><a href="/">Home</a></li>
  <li><a href="/projects">Projects</a></li>
  <li><a class="active" href="/contact">Contact</a></li>
  <li><a href="/resume.pdf">Résumé</a></li>
</ul>
<script>
function showAnswer() {
  var weight=document.getElementById("x").value;
  var height=document.getElementById("y").value;
  var bmi=(weight/(height*height))*10000;
  document.getElementById("ans").innerHTML ="Bmi: " + bmi.toFixed(1);
   if (bmi<18.5)
    document.getElementById("rating").innerHTML = "Underweight";
  else if (bmi<25)
    document.getElementById("rating").innerHTML = "Normal Weight";
  else if (bmi<30)
      document.getElementById("rating").innerHTML = "Overweight";
  else if (bmi>=30)
      document.getElementById("rating").innerHTML = "Obese";
}
</script>
<h1>BMI Calculator</h1>
Weight (kg) <input type="text" name="weight" value="" id="x"><br>
Height (cm) <input type="text" name="height" value="" id="y"><br>
<p id="ans">Bmi: </p>
<p id="rating"></p>
<button type="button" onclick="showAnswer()">Formulate</button>
</body>
</html>
