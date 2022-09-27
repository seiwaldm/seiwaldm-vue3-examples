<script setup>
import { ref } from "vue";

const user = ref({
  name: "Johnny",
  age: 32,
  gender: "",
  checkedAnimals: [],
});

const userList = ref([]);

function addUser() {
  userList.value.push(user.value);
  user.value = { name: "", age: 0, gender: "", checkedAnimals: [] };
}
</script>

<template>
  <h1>Hello World!</h1>
  <p>{{ user.name }} is {{ user.age }} years old!</p>
  <p>{{ user.gender }} loves {{ user.checkedAnimals }}</p>
  <input type="text" v-model="user.name" />
  <input type="number" v-model="user.age" />
  <div>
    <input type="radio" id="male" value="He" v-model="user.gender" />
    <label for="male">Male</label>

    <input type="radio" id="female" value="She" v-model="user.gender" />
    <label for="female">Female</label>
  </div>
  <div>
    <input type="checkbox" id="pig" value="🐷" v-model="user.checkedAnimals" />
    <label for="pig">pig</label>

    <input type="checkbox" id="cow" value="🐮" v-model="user.checkedAnimals" />
    <label for="cow">cow</label>

    <input
      type="checkbox"
      id="horse"
      value="🐴"
      v-model="user.checkedAnimals"
    />
    <label for="horse">horse</label>
  </div>
  <button @click="addUser">Add user to the list</button>
  <ul v-for="item in userList">
    <li>{{ item.name }}</li>
  </ul>
</template>
