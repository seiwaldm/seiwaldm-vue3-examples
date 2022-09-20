<script setup>
import { ref } from 'vue';

const color = ref('red');
const circle = ref(false);
</script>

<template>
  <h2>Colors.vue</h2>
  <h3>Guess a html color name!</h3>
  <input type="text" v-model="color" />
  <div
    class="output"
    :style="{ background: color }"
    :class="{ circle: circle }"
  ></div>
  <button @click="circle = false">Square</button>
  <button @click="circle = true">Circle</button>
</template>

<style scoped>
.output {
  width: 50px;
  aspect-ratio: 1;
  border: 1px solid white;
  margin: 10px auto;
}
.circle {
  border-radius: 50%;
}

button {
  margin: 5px;
}
</style>
