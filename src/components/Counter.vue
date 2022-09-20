<script setup lang="ts">
import { ref } from 'vue';

const counter = ref(0);

function add3() {
  counter.value += 3;
}
</script>

<template>
  <h2>Counter.vue</h2>
  <h3>{{ counter }}</h3>
  <button @click="counter++">Add 1</button>
  <button @click="add3">Add 3</button>
</template>

<style scoped>
button {
  margin: 5px;
}
</style>
