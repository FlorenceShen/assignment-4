<script setup>
const form = document.getElementById('calculate')
import {ref} from 'vue';
  const a = ref(0);
  const b = ref(0);
  const angleC = ref(0) * (Math.PI / 180);

  function Cosine(a, b, angleC) {
    return Math.sqrt(a * a + b * b - 2 * a * b * Math.cos(angleC));
  }
  const result = Cosine(a, b, angleC)
  const resultElement = document.getElementById('result');
  resultElement.style.color = 'black';
  resultElement.innerHTML = result.toFixed(2);
  form.addEventListener('submit', (event) => {
    event.preventDefault();
});
</script>

<template>
<body>
<div class="Cosine box">
          <div class="bold">Cosine Law</div>
          <form id="calculate">
              <label for="sideA"> Side A</label>
              <input type="text" v-model="sideA" name="a">
              <label for="sideB"> Side B</label>
              <input type="text" v-model="sideB" name="b">
              <label for="angleC"> Angle C</label>
              <input type="text" v-model="angleC" name="c">
              <div>Side C(Result):</div>
              <div class="result" id="result"></div>
              <br>
              <button type="submit">Calculate</button>
          </form>
      </div>
      </body>
</template>
