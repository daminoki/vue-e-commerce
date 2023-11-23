<script setup>
import ProductCard from "./ProductCard.vue";
</script>

<template>
  <section class="products">
    <div class="products-container">
      <ProductCard
          title="Apple iPhone 14 Pro Max 128GB Deep Purple (MQ9T3RX/A)"
          imgSrc="./src/assets/img/product-img1.png"
          price="$900"
      />
    </div>
  </section>
</template>

<style scoped lang="scss">
@import "../assets/styles/mixins.scss";

.products-container {
  @include container;

  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 16px;
  padding-top: 120px;
}

</style>