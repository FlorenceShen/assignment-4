<script>
const form2 = document.getElementById('calculate2');
  const m = parseFloat(document.getElementById('mValue').value);
  const n = parseFloat(document.getElementById('nValue').value);
  let resultMessage = "";
  if (m === n)
    resultMessage = "The asymptote is horizontal";
  else if (n > m)
    resultMessage = "The asymptote is the x-axis";
  else {
    const degree = m - n;
    const asymptote = ["Linear", "Quadratic", "Cubic", "Quartic", "Quintic", "Sextic", "Septic", "Octic", "Nonic", "Decic"];
    resultMessage = asymptote[degree - 1];
  }
  const resultElement = document.getElementById('result2');
  resultElement.style.color = 'black';
  resultElement.innerHTML = resultMessage;
  form2.addEventListener('submit', (event) => {
    event.preventDefault();
})
</script>

<template>
  <!DOCTYPE html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
      <div class="Asymptote box">
          <div class="bold"> Asymptote Finder </div>
          <form id="calculate2">
              <label for="mValue"> m value</label>
              <input type="text" id="mValue" name="m">
              <label for="nValue"> n value</label>
              <input type="text" id="nValue" name="n">
              <div>Asymptote Type(Result):</div>
              <div class="result" id="result2"></div>
              <br>
              <button type="submit">Calculate</button>
          </form>
      </div>
      </body>
</template>
