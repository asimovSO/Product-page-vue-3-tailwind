<script setup>
import Offers from "./components/Offers.vue";
import Header from "./components/Header.vue";
import Breadcrumbs from "./components/Breadcrumbs.vue";
import ProductBlock from "./components/ProductBlock.vue";
import Suggestions from "./components/Suggestions.vue";
import DashedLine from "./components/DashedLine.vue";
import ReviewsBlock from "./components/ReviewsBlock.vue";
import Footer from "./components/Footer.vue";

</script>

<template>
  <div class="">
    <Offers />
    <Header />
    <Breadcrumbs />
    <ProductBlock />
    <div class="container"><dashed-line /></div>
    <Suggestions name="Related products" />
    <div class="container"><dashed-line /></div>
    <ReviewsBlock />
    <div class="container">
      <dashed-line />
    </div>
    <Suggestions name="Popular this week" />
    <div class="container">
      <Footer />
    </div>
  </div>
</template>

<style scoped>
</style>
