<template>
  <HelloWorld :user="user" />

  <input type="text" v-model="user.name" @change="display" />
  <input type="text" v-model="user.age" />
</template>

<script setup>
import HelloWorld from "@/components/HelloWorld.vue";
import { reactive } from "vue";

const user = reactive({
  name: "NordCoders",
  age: 30,
});

const display = () => {
  console.log(user.name, user.age);
};

display();
</script>

<style scoped></style>
