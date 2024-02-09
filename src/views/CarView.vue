<script setup>
import { useRoute, useRouter, RouterView } from "vue-router";
import cars from "../data/cars.json";

const route = useRoute();
const router = useRouter();
const carId = parseInt(route.params.id)
const car = cars.find(c => c.id === carId);
</script>

<template>
  <div v-if="car">
    <h1>car view</h1>
    <p>{{ car.name }}</p>
    <p>{{ car.year }}</p>
    <p>{{ car.price }}</p>
    <button @click="router.push(`/cars/${carId}/contact`)">click</button>
    <RouterView />
  </div>
  <div v-else>
    <h1>car not fount</h1>
  </div>
</template>

<style scoped></style>
