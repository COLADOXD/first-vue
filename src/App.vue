<script setup lang="ts">

const name = "Vue dinamico";

const handleClick = () => {
  console.log("Click");
}
</script>

<template>
  <h1>
    Hola {{ name.toUpperCase() }}
  </h1>
  <button @click="handleClick()">active</button>
</template>

<style>
h1 {
  color: red;
}
</style>