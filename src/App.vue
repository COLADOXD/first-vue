<script setup lang="ts">

const name = "Vue dinamico";

const fruitArray = [
  {
    name: "Manzana",
    price: "$1.00",
    description: "Una manzana",
    stock: 0,
  },
  {
    name: "Pera",
    price: "$2.00",
    description: "Una pera",
    stock: 10,
  },
  {
    name: "Naranja",
    price: "$3.00",
    description: "Una naranja",
    stock: 20,
  },
];
</script>

<template>
  <h1>
    Hola {{ name.toUpperCase() }}
  </h1>
  <p>{{ fruitArray }}</p>
  <ul>
    <li v-for="(fruit, index) in fruitArray" :key="fruit.name">{{ fruit.stock }} - {{ fruit.name }} - {{ fruit.price }} :
      {{ fruit.description }}
    </li>
  </ul>
</template>

<style>
h1 {
  color: red;
}
</style>