<script>
import { ref } from 'vue';
  const m = ref();
  const n = ref();
  let resultMessage = ref("");

  function asymptoteFinder(){
  if (m.value === n.value)
    resultMessage.value = "The asymptote is horizontal";
  else if (n.value > m.value)
    resultMessage.value = "The asymptote is the x-axis";
  else {
    const degree = m.value - n.value;
    const asymptote = ["Linear", "Quadratic", "Cubic", "Quartic", "Quintic", "Sextic", "Septic", "Octic", "Nonic", "Decic"];
    resultMessage.value = asymptote[degree - 1];
  }
  }
</script>

<template>
      <div class="Asymptote box">
          <div class="bold"> Asymptote Finder </div>
          <form  @submit.prevent="asymptoteFinder()" id="calculate2">
              <label for="mValue"> m value</label>
              <input type="text" v-model="m" name="m">
              <label for="nValue"> n value</label>
              <input type="text" v-model="n" name="n">
              <div>Asymptote Type(Result):</div>
              <input class="result" v-model="resultMessage" readonly></input>
              <br>
              <button type="submit">Calculate</button>
          </form>
      </div>
</template>
