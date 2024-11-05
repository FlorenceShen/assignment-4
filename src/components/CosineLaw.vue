<script>
const form = document.getElementById('calculate')

  event.preventDefault();
  const a = parseFloat(document.getElementById('sideA').value);
  const b = parseFloat(document.getElementById('sideB').value);
  const angleC = parseFloat(document.getElementById('angleC').value) * (Math.PI / 180);

  function Cosine(a, b, angleC) {
    return Math.sqrt(a * a + b * b - 2 * a * b * Math.cos(angleC));
  }
  const result = Cosine(a, b, angleC)
  const resultElement = document.getElementById('result');
  resultElement.style.color = 'black';
  resultElement.innerHTML = result.toFixed(2);
  form.addEventListener('submit', (event) => {
});
</script>

<template>
<div class="Cosine box">
          <div class="bold">Cosine Law</div>
          <form id="calculate">
              <label for="sideA"> Side A</label>
              <input type="text" id="sideA" name="a">
              <label for="sideB"> Side B</label>
              <input type="text" id="sideB" name="b">
              <label for="angleC"> Angle C</label>
              <input type="text" id="angleC" name="c">
              <div>Side C(Result):</div>
              <div class="result" id="result"></div>
              <br>
              <button type="submit">Calculate</button>
          </form>
      </div>
</template>
<style>
</style>