<script setup lang="ts">

const name = "Vue dinamico";

const arrayFrutas = [
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
  <p>{{ arrayFrutas }}</p>
  <ul>
    <template v-for="(item, index) in arrayFrutas" :key="item.name">
      <li v-if="item.stock > 0">
        {{ item.name }} {{ item.price }}
      </li>
    </template>
  </ul>
</template>

<style>
h1 {
  color: red;
}
</style>