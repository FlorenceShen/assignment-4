<script>
import { ref } from 'vue';
const n2 = ref(0);
let sum = 0;

for (let i = 0; i <= n2; i++) {
  sum += (i % 2 === 0 ? 1 : -1) / (2 * i + 1);
}

const result3 = 4 * sum;
const resultElement = document.getElementById('result3');
resultElement.style.color = 'black';
resultElement.innerHTML = result3.toFixed(8);
form3.addEventListener('submit', (event) => {
  event.preventDefault();
})
</script>

<template>
  <body>
    <div class="Gregory">
      <div class="bold">Gregory-Leibniz Pi Approximation</div>
      <form id="calculate3">
        <label for="nValue2"> n value</label>
        <input type="text" v-model="nValue2" name="n2">
        <div>Pi Approximation(Result):</div>
        <div class="result grey" id="result3">result</div>
        <br>
        <button type="submit">Calculate</button>
      </form>
    </div>
  </body>
</template>
