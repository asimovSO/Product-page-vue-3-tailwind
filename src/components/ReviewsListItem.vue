<template>
<div>
    <div>
    <div class="flex gap-2 mb-3">
      <img
        v-for="(star, idx) in 5"
        :key="idx"
        src="/icons/star.svg"
        alt="star"
        :class="star <= rating ? 'opacity-100' : 'opacity-40 grayscale-50'"
      />
    </div>
    <div class="mb-6">
      <p class="font-semibold text-[18px] text-gray-700 mb-1">
        {{ text_review }}
      </p>
      <span class="block font-light text-gray-500 text-[16px]">{{
        date_review
      }}</span>
    </div>
    <div class="flex justify-between items-center">
      <div class="flex items-center gap-2">
        <img
          :src="avatar_review"
          alt=""
          srcset=""
          class="aspect-square h-8 bg-gray-400 rounded-full"
        />
        <span>{{ author_review }}</span>
      </div>
      <div class="flex gap-6 items-center">
        <button class="flex items-center gap-1">
          <img src="/icons/like.svg" alt="like" />
          <span>{{ likes }}</span>
        </button>
        <button class="flex items-center gap-1" >
          <img src="/icons/like.svg" alt="like" class="scale-x-[-1] rotate-180"/>
        </button>
      </div>
    </div>
  </div>
  <slot></slot>
</div>
</template>
<script setup>
defineProps({
  rating: {
    type: Number,
    required: true,
  },
  text_review: {
    type: String,
  },
  author_review: {
    type: String,
  },
  avatar_review: {
    type: String,
  },
  likes: {
    type: Number,
    default: 0,
  },
  dislikes: {
    type: Number,
    default: 0,
  },
  date_review: {
    type: String,
  },
});
</script>