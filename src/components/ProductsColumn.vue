<script setup>
 import Product from '@/components/Product.vue'
 import uiButton from "@/components/UI/Button.vue"

 import {ref} from 'vue'

 const products = ref([
    {
      id: 1,
      img: '/img/collection-1.jpg',
      title: 'The Dandy chair',
      price: 250
    },
    {
      id: 2,
      img: '/img/collection-2.jpg',
      title: 'Rustic Vase',
      price: 150
    },
    {
      id: 3,
      img: '/img/collection-4.jpg',
      title: 'The Kandy chair',
      price: 250
    },
    {
      id: 4,
      img: '/img/collection-5.jpg',
      title: 'The Dandy ',
      price: 350
    },
    ])
</script>

<template>
  <div class="products-container">
  <div class="products">
    <Product 
        v-for="product of products" 
        :key="product.id"
        :img="product.img"
        :title="product.title"
        :price="product.price"
    />
  </div>
  <div class="products-link">
    <ui-button 
        color="lightgray"
        type="link"
        to="/"
        class="products-link"
        >
        View collection
      </ui-button>
    </div>
  <!-- <a href="#" class="products-link">View collection</a> -->
</div>
</template>

<style lang="scss" scoped>
  .products {
    padding: 0 80px;
    display: flex;
    grid-template-columns: repeat(4, 1fr);
    column-gap: 40px;
    margin-bottom: 64px;
    &-container {
      margin-bottom: 56px;
    }
    &-link{
      // display: block;
      text-align: center;
      // color: #2a254b;
      // text-decoration: none;
      // &:hover{
      //   text-decoration: underline;
      // }
    }
  }
</style>