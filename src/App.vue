<script setup lang="ts">
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import Counter from "./components/Counter.vue";
import Colors from "./components/Colors.vue";
import User from "./components/User.vue";
import { ref } from "vue";

const display = ref(1);
</script>

<template>
  <div>
    <h3>Choose an example:</h3>
    <button @click="display = 1" :class="{ active: display === 1 }">
      simple binding
    </button>
    <button @click="display = 2" :class="{ active: display === 2 }">
      class and style binding, v-model
    </button>
    <button @click="display = 3" :class="{ active: display === 3 }">
      v-model with different input fields & list rendering
    </button>
  </div>
  <hr />
  <Counter v-if="display === 1"></Counter>
  <Colors v-if="display === 2"></Colors>
  <User v-if="display === 3"></User>
</template>

<style scoped>
button {
  display: block;
  margin: 5px auto;
}

.active {
  border: 2px solid white;
}

hr {
  margin: 30px;
}
</style>
