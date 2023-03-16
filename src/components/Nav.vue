<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  
  <nav>
    <RouterLink active-class="active" to="/">Home</RouterLink>
    <RouterLink active-class="active" to="/about">About</RouterLink>
  </nav>
</template>

<style scoped>
.active {
  font-weight: 900;
  color: rgb(127, 150, 255);
}

</style>
