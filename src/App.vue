<script setup>
import CosineLaw from './components/CosineLaw.vue'
import AsymptoteFinder from './components/AsymptoteFinder.vue'
import GregoryLeibnizPi from './components/GregoryLeibnizPi.vue'
</script>

<template>
<!DOCTYPE html>
  <head>
      <meta charset="UTF-8">
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      <title>Document</title>
  </head>
  <CosineLaw/>
  <AsymptoteFinder/>
  <GregoryLeibnizPi/>
</template>

<style scoped>
body {
  background: linear-gradient(to right, #e0e9fa, #ffffff);
  font-family: "Poppins", sans-serif;
}

.box {
  display: flex;
}

.bold {
  font-weight: bold;
}

label {
  display: flex;
  flex-direction: column;
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
  display: flex;
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
