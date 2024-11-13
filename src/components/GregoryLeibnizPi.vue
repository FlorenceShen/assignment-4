<script setup>
import { ref } from 'vue';
const n2 = ref(0);
let sum = ref(0);
let i = ref(0)
let result = ref(0)

function gregory(){
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
