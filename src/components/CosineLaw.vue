<script setup>
import { ref } from 'vue';
const a = ref();
const b = ref();
const angleC = ref();
const c = ref();

function cosine() {
  c.value = Math.round(Math.sqrt(a.value * a.value + b.value * b.value - 2 * a.value * b.value * Math.cos(angleC.value * (Math.PI / 180)))).toFixed(2);
}
</script>

<template>
  <div class="Cosine box">
    <div class="bold">Cosine Law</div>
    <form @submit.prevent="cosine()">
      <label for="sideA"> Side A</label>
      <input type="text" v-model="a" name="a">
      <label for="sideB"> Side B</label>
      <input type="text" v-model="b" name="b">
      <label for="angleC"> Angle C</label>
      <input type="text" v-model="angleC" name="c">
      <div>Side C(Result):</div>
      <input class="result" v-model="c" readonly></input>
      <br>
      <button type="submit">Calculate</button>
    </form>
  </div>
</template>
