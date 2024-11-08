<script>
const form2 = document.getElementById('calculate2');
  const m = ref(0);
  const n = ref(0);
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
<body>
      <div class="Asymptote box">
          <div class="bold"> Asymptote Finder </div>
          <form id="calculate2">
              <label for="mValue"> m value</label>
              <input type="text" v-model="mValue" name="m">
              <label for="nValue"> n value</label>
              <input type="text" v-model="nValue" name="n">
              <div>Asymptote Type(Result):</div>
              <div class="result" id="result2"></div>
              <br>
              <button type="submit">Calculate</button>
          </form>
      </div>
      </body>
</template>
