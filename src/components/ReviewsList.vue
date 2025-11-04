<template>
  <div>
    <h5 class="text-xl font-semibold block mb-4">Reviews List</h5>
    <div class="reviews-tabs flex items-center gap-6 cursor-pointer text-sm font-semibold">
      <div
        v-for="(tab, idx) in tabs"
        :key="idx"
        @click="setTab(idx)"
        class="py-2.5 px-5 transition-all duration-300 ease-in-out"
        :class="{ 'border border-black rounded': activeTab == idx, 'border border-transparent': activeTab != idx }"
      
      >
        {{ tab }}
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref } from "vue";

const tabs = ref(["All Reviews", "With Photos", "With Videos"]);
const activeTab = ref(0);
function setTab(idx) {
  activeTab.value = idx;
}
</script>