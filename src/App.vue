<script setup>
 import Header from '@/components/Layout/Header.vue'
 import Footer from '@/components/Layout/Footer.vue'
</script>

<template>
  <div class="container">
    <Header />
    <RouterView></RouterView>
    <Footer />
  </div>
</template>

<style lang="scss">
  @import url('https://fonts.cdnfonts.com/css/satoshi');
  @import url('https://fonts.cdnfonts.com/css/clash-display');
  

  * {
  box-sizing: border-box;
  font-weight: 400;
  }

body {
    margin: 0;
    padding: 0;
    font-family: 'Satoshi', sans-serif;
    font-size: 16px;
    color: #22202e;
    // font-family: 'Clash Display', sans-serif;                                              
  }
img {
  max-width: 100%;
}
.container {
    max-width: 1440px;
    margin: auto;
    padding: 0 24px;
  }
.input-text {
  height: 56px;
  padding: 0 32px;
  font-size: 16px;
  border: none;
}
</style>
