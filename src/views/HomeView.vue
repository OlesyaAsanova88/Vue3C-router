<script setup>

import { RouterLink} from 'vue-router'
import cars from "../data/cars.json"
</script>

<template>
  <main>
    <h1>Home catalog cars</h1>
    <div class="cars">
      <RouterLink :to="`/car/${car.id}`" v-for="car in cars" :key="car.id" href="">
        {{ car.name }}
      </RouterLink>
    </div>
  </main>
</template>

<style scoped>
.cars {
  display: flex;
 
}
.cars a {
  margin-top: 30px;
  text-decoration: none;
  width: 100%;
  font-weight: 700;
  box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.199);
  margin-left: 20px;
}
</style>
