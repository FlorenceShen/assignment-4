<script setup>
import CosineLaw from './components/CosineLaw.vue'
import AsymptoteFinder from './components/AsymptoteFinder.vue'
import GregoryLeibnizPi from './components/GregoryLeibnizPi.vue'
</script>

<template>
  <div class="box">
    <CosineLaw/>
    <AsymptoteFinder/>
    <GregoryLeibnizPi/>
  </div>
</template>

<style scoped>
.box{
  display: flex;
  justify-content: flex-start;
  flex-wrap: wrap;
}
</style>