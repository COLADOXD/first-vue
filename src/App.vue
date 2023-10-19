<script setup lang="ts">
import { ref } from 'vue';


const name = "Vue dinamico";

let counter = ref(0)

const increment = () => {
  counter.value += 1;
}
</script>

<template>
  <h1>
    Hola {{ name.toUpperCase() }}
  </h1>
  <h2>{{ counter }}</h2>
  <button @click="increment">active</button>
</template>

<style>
h1 {
  color: red;
}
</style>