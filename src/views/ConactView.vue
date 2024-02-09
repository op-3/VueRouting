<script setup>
import { useRoute } from "vue-router";
import cars from "../data/cars.json";
const route = useRoute();

const car = cars.find((c) => c.id === parseInt(route.params.id));
</script>

<template>
  <div>
    <h1>contact info</h1>
    <p>{{ car.contact.dealer }}</p>
    <p>{{ car.contact.number }}</p>
  </div>
</template>

<style scoped></style>
