<template>
  <div
    class="flex flex-col w-fit h-auto cursor-pointer hover:opacity-80 rounded p-2 border border-transparent hover:border-gray-300 transition"
  >
    <img
      :src="imageUrl"
      alt=""
      class="w-full h-full object-cover rounded-lg mb-4"
    />
    <div class="text-lg font-semibold mb-2">{{ name }}</div>
    <div class="text-sm text-slate-500 mb-2">{{ typeofProduct }}</div>
    <div class="text-xl font-bold mb-2">${{ price.toFixed(2) }}</div>
    <div class="flex items-center gap-4 text-sm text-slate-500">
      <div>
        <img src="/icons/star.svg" alt="rate" class="inline-block mr-1" />
        <span class="text-black font-medium text-base">{{ rating }}</span>
      </div>
      <div>Sold: {{ numberOfSold }}</div>
    </div>
  </div>
</template>
<script setup>
defineProps({
  name: String,
  price: Number,
  imageUrl: String,
  rating: Number,
  numberOfSold: Number,
  typeofProduct: String,
});
</script>