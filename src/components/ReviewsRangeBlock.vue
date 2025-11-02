<template>
  <div class="w-full">
    <div
      v-for="(item, idx) in 5"
      :key="idx"
      class="flex items-center gap-3 h-10"
    >
      <div class="flex items-center gap-1.5">
        <img src="/icons/star.svg" alt="star" />
        <span>{{ 5 - idx }}.0</span>
      </div>
      <div class="flex-1">
        <progress
          class="rating-bar appearance-none w-full h-2 rounded bg-slate-200"
          :value="(Math.random() * 100).toFixed(0)"
          max="100"></progress>
      </div>
      <div class="number_reviews">2234</div>
    </div>
  </div>
</template>
<style scoped>

.rating-bar::-webkit-progress-bar {
  background-color: oklch(37.2% 0.044 257.287);
  border-radius: 0.5rem;
}
.rating-bar::-moz-progress-bar{
  background-color: oklch(37.2% 0.044 257.287);
  border-radius: 0.5rem; 
}
</style>