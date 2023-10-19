<script setup lang="ts">
import { ref } from 'vue';


const name = "Vue dinamico";

let counter = ref(0);
</script>

<template>
  <h1>
    Hola {{ name.toUpperCase() }}
  </h1>
  <h2 :style="counter >= 0 ? 'color: green' : 'color: red'">{{ counter }}</h2>
  <button @click="counter++">increment</button>
  <button @click="counter--">reduce</button>
  <button @click="counter = 0">reset</button>
</template>