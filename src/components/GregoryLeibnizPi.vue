<script setup>
import { ref } from 'vue';
const n2 = ref(0);
let sum = ref(0);
let i = ref(0)
let result = ref()

function gregory() {
  for (i.value <= n2.value; i.value++;) {
    sum.value += Math.round(i.value % 2 === 0 ? 1 : -1) / (2 * i.value + 1).toFixed(8);
    return sum.value
  }
  result.value = 4 * sum.value;
}
</script>

<template>
  <div class="Gregory">
    <div class="bold">Gregory-Leibniz Pi Approximation</div>
    <form @submit.prevent="gregory()">
      <label for="nValue2"> n value</label>
      <input type="text" v-model="nValue2" name="n2">
      <div>Pi Approximation(Result):</div>
      <input class="result grey" v-model="result" readonly>result</input>
      <br>
      <button type="submit">Calculate</button>
    </form>
  </div>
</template>

<style>
.box {
  display: flex;
  flex-direction: column;
}

.bold {
  font-weight: bold;
}

label {
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
  margin-top: 5px;
  flex-direction: column;
  font-family: 'Poppins';
  background-color: #ffffff;
  border: 1px solid #919191;
  border-radius: 4px;
}

.Cosine, .Asymptote, .Gregory {
  font-family: "Poppins", sans-serif;
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
  height: 300px;
}

.result {
  font-size: 17px;
  padding: 1px 20px;
  height: 25px;
  background-color: aliceblue;
  border: 1px solid #000000;
  box-sizing: border-box;
  border-radius: 4px;
}

.grey {
  color: rgb(158, 172, 172)
}
</style>
