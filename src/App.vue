<script setup lang="ts">
import { ref, computed, Ref } from 'vue';


const name = "Vue dinamico";

let counter = ref(0);
let counterArray: Ref<number[]> = ref([]);

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

const addNumber = computed(() => {
  const disabled = counterArray.value.find((number) => number === counter.value);
  if (disabled === 0) {
    return true
  }
  return disabled ? true : false
})
</script>

<template>
  <div class="container text-center mt-5">
    <h1>
      Hola {{ name.toUpperCase() }}
    </h1>

    <div class="btn-group">
      <button class="btn btn-success" @click="counter++">increment</button>
      <button class="btn btn-danger" @click="counter--">reduce</button>
      <button class="btn btn-secondary" @click="counter = 0">reset</button>
      <button class="btn btn-primary" :disabled="addNumber" @click="counterArray.push(counter)">add</button>
    </div>
    <h2 :style="counter >= 0 ? 'color: green' : 'color: red'">{{ classComputer }}</h2>
    <h2 :style="counter >= 0 ? 'color: green' : 'color: red'">{{ counter }}</h2>
    <h2>{{ counterArray }}</h2><br>
    <ul class="list-group mt-2">
      <li class="list-group-item" v-for="number in counterArray">
        {{ number }}</li>
    </ul>
  </div>
</template>