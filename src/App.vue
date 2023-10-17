<script setup lang="ts">

const name = "Vue dinamico";

//Cuando se recorre un objeto primero es el valor, propiedad y al ultimo el index
const fruitObj = {
  name: "Manzana",
  price: "$1.00",
  description: "Una manzana",
  stock: 0,
}
</script>

<template>
  <h1>
    Hola {{ name.toUpperCase() }}
  </h1>
  <p>{{ fruitObj }}</p>
  <ul>
    <li v-for="(value, property, index) in fruitObj" :key="value">
      {{ `${index} - ${property}: ${value}` }}
    </li>
  </ul>
</template>

<style>
h1 {
  color: red;
}
</style>