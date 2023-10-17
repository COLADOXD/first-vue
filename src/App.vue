<script setup>
const name = "Vue dinamico";
const colorBlue = "color: blue";

</script>

<template>
  <h1>
    Hola {{ name }}
    <h2 :style="colorBlue">Soy azul</h2>
  </h1>
</template>

<style>
h1 {
  color: red;
}
</style>