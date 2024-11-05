<script>
const form3 = document.getElementById('calculate3');

  event.preventDefault();
  const n2 = parseInt(document.getElementById('nValue2').value);
  let sum = 0;

  for (let i = 0; i <= n2; i++) {
    sum += (i % 2 === 0 ? 1 : -1) / (2 * i + 1);
  }
  
  const result3 = 4 * sum;
  const resultElement = document.getElementById('result3');
  resultElement.style.color = 'black';
  resultElement.innerHTML = result3.toFixed(8);
  form3.addEventListener('submit', (event) => {
})
</script>

<template>
<div class="Gregory">
      <div class="bold">Gregory-Leibniz Pi Approximation</div>
      <form id="calculate3">
          <label for="nValue2"> n value</label>
          <input type="text" id="nValue2" name="n2">
          <div>Pi Approximation(Result):</div>
          <div class="result grey" id="result3">result</div>
          <br>
          <button type="submit">Calculate</button>
      </form>
  </div>
</template>
<style>
</style>