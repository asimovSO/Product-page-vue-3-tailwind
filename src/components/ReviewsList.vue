<template>
  <div>
    <h5 class="text-xl font-semibold block mb-4">Reviews List</h5>
    <div class="flex justify-between">
      <div
        class="reviews-tabs flex flex-wrap md:flex-nowrap items-center gap-6 cursor-pointer text-sm font-semibold"
      >
        <div
          v-for="(tab, idx) in tabs"
          :key="idx"
          @click="setTab(idx)"
          class="py-2.5 px-5 transition-all duration-300 ease-in-out"
          :class="{
            'border border-black rounded': activeTab == idx,
            'border border-transparent rounded': activeTab != idx,
          }"
        >
          {{ tab }}
        </div>
      </div>
      <div class="md:hidden p-1.5">
        <img src="/icons/filter.svg" alt="filter" />
      </div>
    </div>
    <div class="py-8">
      <ReviewsListItem
        v-for="(review, idx) in reviews"
        :key="idx"
        :rating="review.rating"
        :text_review="review.text_review"
        :author_review="review.author_review"
        :avatar_review="review.avatar_review"
        :likes="review.likes"
        :dislikes="review.dislikes"
        :date_review="review.date_review"
      >
      <div class="border-b border-dashed border-slate-300 my-10" v-if='idx !== reviews.length - 1'></div>
      </ReviewsListItem>
    </div>
  </div>
</template>
<script setup>
import { ref } from "vue";
import DashedLineVue from "./DashedLine.vue";
import ReviewsListItem from "./ReviewsListItem.vue";
import DashedLine from "./DashedLine.vue";

const tabs = ref(["All Reviews", "With Photos", "With Videos"]);
const activeTab = ref(0);
function setTab(idx) {
  activeTab.value = idx;
}

const reviews = ref([
  {
    rating: 5,
    text_review:
      "This product is amazing! I've been using it for a few weeks now and it has exceeded my expectations. Highly recommend to anyone looking for quality and reliability.",
    author_review: "John Doe",
    avatar_review: "/img/models/model_second_1.png",
    likes: 12,
    dislikes: 2,
    date_review: "2023-10-15",
  },
  {
    rating: 4,
    text_review:
      "Good value for the price. There are a few minor issues, but overall I'm satisfied with my purchase.",
    author_review: "Jane Smith",
    avatar_review: "/img/models/model_second_1.png",
    likes: 8,
    dislikes: 1,
    date_review: "2023-09-20",
  },
  {
    rating: 1,
    text_review:
      "Not what I expected. The quality is subpar and it didn't work as advertised. Would not buy again.",
    author_review: "Mike Johnson",
    avatar_review: "/img/models/model_second_1.png",
    likes: 3,
    dislikes: 5,
    date_review: "2023-08-10",
  },
  {
    rating: 5,
    text_review:
      "Absolutely love it! The design is sleek and it performs exceptionally well. I've received many compliments on it.",
    author_review: "Emily Davis",
    avatar_review: "/img/models/model_second_1.png",
    likes: 15,
    dislikes: 0,
    date_review: "2023-07-05",
  },
]);
</script>