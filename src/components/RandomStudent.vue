<script setup>
import { ref } from "vue";

const students = ref([
  {
    number: 1,
    name: "Migei",
    hobbies: ["Tennis", "Skifahren"],
  },
  {
    number: 2,
    name: "Didi",
    hobbies: ["Gaming"],
  },
  {
    number: 3,
    name: "Gegei",
    hobbies: ["Tennis", "Gaming"],
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
    hobbies: ["Krafttraining"],
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
    hobbies: ["Fußball"],
  },
]);

const klassensprecher = {
  vorname: "Stefan",
  nachname: "Portenkirchner",
  haarfarbe: "braun",
  augenfarbe: "blau",
  größe: "187 cm",
  gewicht: "77 kg",
};
</script>

<template>
  <h2>RandomStudent.vue</h2>
  <h3>v-for mit Arrays</h3>
  <ol>
    <li v-for="student in students" :key="student.number">
      {{ student.name }}
      <ul v-if="student.hobbies">
        <li v-for="hobby in student.hobbies">
          {{ hobby }}
        </li>
      </ul>
    </li>
  </ol>
  <h3>v-for mit einem Objekt</h3>
  <ul>
    <li v-for="(value, key) in klassensprecher">{{ key }}: {{ value }}</li>
  </ul>
</template>
