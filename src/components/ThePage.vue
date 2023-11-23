<script setup>
  import TheHeader from "./TheHeader.vue";
  import SvgSprite from "./SvgSprite.vue";
  import ProductsList from "./ProductsList.vue";
</script>

<template>
  <div class="page-container">
    <TheHeader />
    <main class="page">
      <ProductsList />
    </main>
    <SvgSprite />
  </div>
</template>

<style scoped>
</style>