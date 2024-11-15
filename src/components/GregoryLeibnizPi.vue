<script setup>
import { ref } from 'vue';
const n2 = ref();
const result = ref();

function gregory() {
  let sum = 0;
  for (let i = 0; i <= n2.value; i++) {
    sum += (i % 2 === 0 ? 1 : -1) / (2 * i + 1);
  }
  result.value = (4 * sum).toFixed(8);
}
</script>

<template>
  <div class="Gregory">
    <div class="bold">Gregory-Leibniz Pi Approximation</div>
    <form @submit.prevent="gregory()">
      <label for="nValue2"> n value</label>
      <input type="text" v-model="n2" name="n2">
      <div>Pi Approximation(Result):</div>
      <input class="result" :value="result" readonly></input>
      <br>
      <button type="submit">Calculate</button>
    </form>
  </div>
</template>

<style>
.bold {
  font-weight: bold;
}

label {
  flex-direction: column;
  display: flex;
}

input {
  font-size: 15px;
  border-radius: 4px;
  border: 1px solid #7e7e7e;
}

button:hover {
  background-color: #bebebe;
  cursor: pointer;
}

button {
  font-family: "Poppins", sans-serif;
  margin-top: 5px;
  flex-direction: column;
  background-color: #ffffff;
  border: 1px solid #919191;
  border-radius: 4px;
}

.Cosine, .Asymptote, .Gregory {
  font-family: "Poppins", sans-serif;
  flex-direction: column;
  width: 40%;
  padding: 12px 20px;
  margin: 8px 15px 0;
  background-color: #abc2e0;
  border: 1px solid #9e9e9e;
  border-radius: 4px;
  box-sizing: border-box;
  box-shadow: 0 8px 20px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgb(150, 150, 150);
}

.Gregory {
  height: 250px;
}

.result {
  font-size: 17px;
  padding: 1px 20px;
  height: 25px;
  background-color: aliceblue;
  border: 1px solid #5a5858;
  box-sizing: border-box;
  border-radius: 4px;
}
</style>
