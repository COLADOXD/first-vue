<script setup lang="ts">
import { ref } from 'vue';

const name = "Vue dinamico";
const active = null;

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
  <p v-if="active">Active</p>
  <p v-else-if="active === false">Don't active</p>
  <p v-else>Estoy indeciso</p>
  <h2 @click="colorChange()" :style="`color: ${num}`">Soy {{ num }}</h2>
  <h2 v-show="active">active</h2>
</template>

<style>
h1 {
  color: red;
}
</style>