<script setup>
import Offers from "./components/Offers.vue";
import Header from "./components/Header.vue";
import Breadcrumbs from "./components/Breadcrumbs.vue";
import ProductBlock from "./components/ProductBlock.vue";
import Suggestions from "./components/Suggestions.vue";
import DashedLine from "./components/DashedLine.vue";
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
  </div>
</template>

<style scoped>
</style>
