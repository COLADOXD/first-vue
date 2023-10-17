<script setup lang="ts">
import { ref } from 'vue';

const name = "Vue dinamico";
const active = true;

let num = ref('');

const colorArray = ['blue', 'green', 'black'];
let count = 0;
const colorChange = () => {
  count = (count + 1) % colorArray.length;
  num.value = colorArray[count];
}


colorChange()
</script>

<template>
  <h1>
    Hola {{ name.toUpperCase() }}
  </h1>
  <p>{{ active ? "I'm active" : "Don't active" }}</p>
  <h2 @click="colorChange()" :style="`color: ${num}`">Soy {{ num }}</h2>
</template>

<style>
h1 {
  color: red;
}
</style>