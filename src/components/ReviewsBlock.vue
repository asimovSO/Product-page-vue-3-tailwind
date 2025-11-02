<template>
  <div class="container">
    <div class="mb-6">
      <span class="text-2xl font-bold">Product Reviews</span>
    </div>
    <div
      class="h-[300px] w-full grid md:grid-cols-8 md:justify-between gap-2 md:gap-5"
    >
      <div class="1 md:col-span-8 flex items-start justify-between border border-slate-300 border-dashed p-6 rounded">
        <div class="flex items-center gap-4 w-full">
          <div
            class="rate-number w-fit p-6 rounded-full border-4 border-orange-300 text-xl font-semibold"
          >
            4.5
          </div>
          <div>
            <div class="flex gap-1 mb-2">
              <img src="/icons/star.svg" alt="r star" />
              <img src="/icons/star.svg" alt="r star" />
              <img src="/icons/star.svg" alt="r star" />
              <img src="/icons/star.svg" alt="r star" />
              <img src="/icons/star.svg" alt="r star" />
              <br />
            </div>
            <span class="text-slate-500 text-sm block">from 1,25k reviews</span>
          </div>
        </div>

        <reviews-range-block class=""/>

      </div>
      <div class="2 border border-red-700 md:col-span-6"></div>
    </div>
  </div>
</template>
<script setup>
import ReviewsRangeBlock from "./ReviewsRangeBlock.vue";
</script>