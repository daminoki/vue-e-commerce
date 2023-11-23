<script setup>
defineProps(['title', 'imgSrc', 'price']);
</script>

<template>
  <div class="product">
    <div class="product-favorites">
      <svg width="32" height="32">
        <use href="#card-favorite" />
      </svg>
    </div>

    <div class="product-img">
      <img :src="imgSrc" alt="Изображение продукта">
    </div>

    <div class="product-content">
      <h3 class="product-title">{{ title }}</h3>
      <p class="product-price">{{ price }}</p>
      <button type="button" class="product-button">Buy Now</button>
    </div>
  </div>
</template>

<style scoped lang="scss">
@import "../assets/styles/mixins.scss";

.product {
  padding: 24px 16px;
  background-color: var(--light-grey);
  border-radius: 8px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 16px;
}

.product-favorites {
  margin-left: auto;
}

.product-img {
  width: 160px;
  height: 160px;

  img {
    display: block;
    width: 100%;
    height: 100%;
    object-fit: contain;
  }
}

.product-content {
  display: flex;
  flex-direction: column;
}

.product-title {
  @include txt-16-medium;
  text-align: center;
}

.product-price {
  @include txt-24-semi-bold;
  margin-top: 16px;
  text-align: center;
}

.product-button {
  @include txt-14-medium;

  color: var(--typo-light);
  padding: 12px 64px;
  background-color: #000;
  border-radius: 8px;
  margin: 24px auto 0;
}
</style>