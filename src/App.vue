<script setup lang="ts">
import { ref, computed } from 'vue';


const name = "Vue dinamico";

let counter = ref(0);

const classComputer = computed(() => {
  if (counter.value === 0) {
    return 'zero'
  }
  if (counter.value > 0) {
    return 'positive'
  }
  if (counter.value) {
    return 'negative'
  }
});
</script>

<template>
  <h1>
    Hola {{ name.toUpperCase() }}
  </h1>
  <h2 :style="counter >= 0 ? 'color: green' : 'color: red'">{{ classComputer }}</h2>
  <h2 :style="counter >= 0 ? 'color: green' : 'color: red'">{{ counter }}</h2>
  <button @click="counter++">increment</button>
  <button @click="counter--">reduce</button>
  <button @click="counter = 0">reset</button>
  <button :disabled="false">add</button>
</template>