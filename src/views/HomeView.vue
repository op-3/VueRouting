<script setup>
import cars from "../data/cars.json";
import { RouterLink } from "vue-router";
</script>

<template>
  <div>
    <h1>home view</h1>
    <div class="cars">
      <RouterLink :to="`/cars/${car.id}`" v-for="car in cars" :key="car.id" href=""> {{ car.name }}</RouterLink>
    </div>
  </div>
</template>

<style scoped>
.cars {
  display: flex;
}

.cars a {
  text-decoration: none;
  color: white;
  width: 100%;
  box-shadow: 1px 1px 2px 2px rgba(255, 255, 255, 0.414);
  margin: 10px;
}
</style>
