<script setup>
import {useRoute, useRouter, RouterView } from 'vue-router'
import cars from "../data/cars.json"

const route = useRoute()
const router = useRouter()

const carId =  parseInt(route.params.id)

const car = cars.find(c => c.id === carId)

</script>

<template>
    <div v-if="car">
        <h1>CarView</h1>
        <p>{{ car.name }}</p>
        <p>{{ car.year }}</p>
        <p>{{ car.price }}</p>
        
        <img :src="car.img" alt="">

        <p>{{ car.contact.dealer }}</p>
        <p>{{ car.contact.number }}</p> 

        <button class="back-home">
            <RouterLink class="back-home__link"  to="/">Вернуться к списку машин</RouterLink>
            </button>
    </div>
    <div v-else>
        <h2>Car note found</h2>
    </div>
</template>

<style scoped>
    .back-home {
        margin-top: 20px;
        padding: 8px 15px;
        border-radius: 5px;
        border: none;
        box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.171);
    }
    .back-home:hover {
        
        background-color: #a18b5052;
    }
    .back-home__link {
        font-family: 'Prata', sans-serif;
        text-decoration: none;
        color: black;
        font-weight: 500;
    }
   
</style>