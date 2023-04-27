<script setup>
 const props = defineProps({
  img: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  price: {
    type: Number,
    required: true
  },
 })
</script>

<template>
  <div class="product">
    <router-link to="/product">
      <img :src="img" :alt="title" class="product-image">
    </router-link>
    <router-link to="/" class="product-name">{{ title }}</router-link>
    <span class="product-price">{{ price }}</span>
  </div>
</template>

<style lang="scss" scoped>
  .product {
    &-image {
      display: block;//viravnivaet img do odinakovoi
      margin-bottom: 24px;
    }
    &-name {
      display: block;
      color: #2a254b;
      font-size: 20px;
      line-height: 20px;
      font-family: 'Clash Display', sans-serif; 
      margin-bottom: 8px;
    }
    &-price {
      display: block;
  }}
</style>