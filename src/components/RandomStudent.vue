<script setup>
import { ref } from "vue";

const students = ref([
  {
    number: 1,
    name: "Migei",
  },
  {
    number: 2,
    name: "Didi",
  },
  {
    number: 3,
    name: "Gegei",
  },
  {
    number: 4,
    name: "Viki",
  },
  {
    number: 5,
    name: "Patrick",
  },
  {
    number: 6,
    name: "Portei",
  },
  {
    number: 7,
    name: "Eli",
  },
  {
    number: 8,
    name: "Seppi",
  },
  {
    number: 9,
    name: "Mani",
  },
]);
</script>

<template>
  <h2>RandomStudent.vue</h2>
  <ul>
    <li v-for="student in students" :key="student.number">
      {{ student.name }}
    </li>
  </ul>
</template>
