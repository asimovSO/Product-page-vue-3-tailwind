<template>
    <div class="container">
        <div class="flex justify-between items-center my-4">
            <span class="text-2xl font-bold"> {{name}} </span>
            <a href="#" class="underline font-light">View all</a>
        </div>
        <div class="flex justify-evenly md:justify-between flex-wrap md:flex-nowrap gap-6">
            <ProductCard
            v-for='(item, idx) in 5'
            :key="idx"
            name="Long Sleeve Overshirt, Khaki, 6"
            :price="59.99"
            imageUrl="/img/models/model_second_1.png"
            :rating="4.5"
            :numberOfSold="120"
            typeofProduct="Shirts & Tops"
        />
        </div>
    </div>
</template>
<script setup>
import ProductCard from './ProductCard.vue'
import { ref } from "vue";

defineProps({
    name: String
})
</script>