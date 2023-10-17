<script setup lang="ts">

const name = "Vue dinamico";

const fruitArray = ["🍉", "🍊", "🍋", "🍌", "🍍", "🥭"]
</script>

<template>
  <h1>
    Hola {{ name.toUpperCase() }}
  </h1>
  <p>{{ fruitArray }}</p>
  <ul>
    <li v-for="(fruit, index) in fruitArray" :key="index">{{ index }} - {{ fruit }}</li>
  </ul>
</template>

<style>
h1 {
  color: red;
}
</style>