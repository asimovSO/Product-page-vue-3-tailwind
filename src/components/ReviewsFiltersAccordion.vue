<template>
  <div class="w-full">
    <div class="flex justify-between mb-3 cursor-pointer" @click="toggleAcc">
      <span class="block text-base font-semibold">{{ filterTitle }}</span>
      <img class="block" src="/icons/arrow-down.svg" alt="open" v-if="isOpen" />
      <img
        class="block"
        src="/icons/arrow-down.svg"
        alt="open"
        style="transform: rotate(180deg)"
        v-else
      />
    </div>

    <Transition
      enter-from-class="max-h-0 opacity-0 overflow-hidden"
      enter-to-class="max-h-96 opacity-100"
      enter-active-class="transition-all duration-300 ease-in-out"
      leave-from-class="max-h-96 opacity-100"
      leave-to-class="max-h-0 opacity-0 overflow-hidden"
      leave-active-class="transition-all duration-300 ease-in-out"
    >
      <div v-show="isOpen">
        <div class="items" v-for="(item, idx) in arrayItems" :key="idx">
          <input type="checkbox" name="filter-check" id=""  class="mr-2"/>
          <label for="filter-check" class="text-base text-slate-500">{{ item }}</label>
        </div>
      </div>
    </Transition>
  </div>
</template>
<script setup>
import { ref } from "vue";

const isOpen = ref(true);
const toggleAcc = () => {
  isOpen.value = !isOpen.value;
};

defineProps({
  filterTitle: {
    type: String,
    default: "Filter",
    required: true
  },
  arrayItems: {
    type: Array,
    default: () => [],
  },
});
</script>