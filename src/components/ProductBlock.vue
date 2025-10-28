<template>
  <div class="container">
    <div class="flex justify-between">
      <div class="flex-1">
        <img src="/img/models/model_main.png" alt="" srcset="" />
      </div>
      <div class="flex-1">
        <div class="text-3xl font-bold mb-3">
          <h1>Long Sleeve Overshirt, Khaki, 6</h1>
        </div>
        <div class="flex justify-between">
          <div class="price-block">
            <span
              class="old-price line-through text-gray-500 text-base inline-block align-middle mr-2"
              >£40.00</span
            >
            <span
              class="current-price text-2xl font-bold inline-block align-middle"
              >£28.00</span
            >
          </div>
          <div class="product-rating flex items-center gap-2">
            <span class="text-slate-500 mr-2">1236 sold</span>
            <img src="/icons/star.svg" alt="Star" />
            <span class="font-medium">4.5</span>
          </div>
        </div>
        <div class="border-b border-dashed border-slate-300 my-7 h-px"></div>
        <div class="details-block">
          <div class="desc">
            <p class="font-semibold">Description:</p>
            <p class="text-gray-500">
              Boba etiam ut bulla tea est potus dilectus singulari compositione
              saporum et textuum, quae in Taiwan annis 1980 orta sunt. Boba
              refert ad pilas masticas tapiocas in fundo potus inventas, quae
              typice lacte tea nigro sapiuntur. Boba phaenomenon.
              <a href="#" class="underline text-black">See More....</a>
            </p>
          </div>
        </div>
        <Picker
          nameOfPicker="Size"
          :isColor="false"
          :valuesToPick="all_sizes"
        />
        <Picker 
          nameOfPicker="Color"
          :isColor="true"
          :valuesToPick="all_colors"
        />
        <div class="flex gap-2 my-10">
          <button class="flex-1 rounded bg-black text-white py-4 font-semibold cursor-pointer active:opacity-25 transition">Add To Cart</button>
          <button class="flex-1 rounded border border-slate-300 py-4 font-semibold cursor-pointer active:opacity-25 transition">Checkout Now</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import Picker from "./Picker.vue";  
import { ref } from "vue";

const all_sizes = ref([
  {
    name: "6",
    value: 6,
  },
  {
    name: "8",
    value: 8,
  },
  {
    name: "10",
    value: 10,
  },
]);

const all_colors = ref([
  {
    name: 'Brown',
    value: '#A52A2A',
  },
  {
    name: 'Black',
    value: '#000000',
  },
  {
    name: 'Olive',
    value: '#808000',
  },
])
</script>