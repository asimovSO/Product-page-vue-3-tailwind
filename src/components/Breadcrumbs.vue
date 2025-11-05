<template>
  <div>
    <div class="container flex flex-wrap items-center my-7 text-slate-500 text-base">
      <div v-for="(breadcrumb, idx) in breadcrumbs" :key="idx" class="flex items-center gap-1">
        <div>{{ breadcrumb.name }}</div >
        <img src='/icons/arrow-right.svg' v-if="idx !== breadcrumbs.length - 1" class="mr-2"/>
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref } from "vue";

const breadcrumbs = ref([
  { name: "Homepage" },
  { name: "Women" },
  { name: "Women Shirts & Tops" },
  { name: "Long Sleeve Overshirt, Khakin, 6" },
]);
</script>