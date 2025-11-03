<template>
  <div class="border border-slate-300 rounded border-dashed p-6 w-full">
    <div>
      <span class="text-xl font-semibold">Reviews Filter</span>
    </div>
    <div class="w-full h-px border-b border-dashed border-slate-300 my-4"></div>
    <div class="flex flex-col gap-5">
      <ReviewsFiltersAccordion filterTitle="Rating" :arrayItems="ratingItems" />
      <ReviewsFiltersAccordion filterTitle="Review Topics" :arrayItems="reviewTopicsItems" />
    </div>
  </div>
</template>
<script setup>
import ReviewsFiltersAccordion from "./ReviewsFiltersAccordion.vue";
import { ref } from "vue";

const ratingItems = ref(["5 stars", "4 stars", "3 stars", "2 stars", "1 star"]);
const reviewTopicsItems = ref([
  "Product Quality",
  "Seller Service",
  "Product Service",
  "Shipment",
  "Matching Description"
]);
</script>