<script setup>
  import HeroInformation from '@/components/HeroInformation.vue';
</script>

<template>
  <div class="hero">
 
      <HeroInformation 
        title="Luxury homeware for people who love timeless design quality"
        description="Shop the new Spring 2022 collection today"
        link="#"
        colorLink="lightgray"
      />

  </div>
</template>

<style lang="scss" scoped>
  .hero{
    background-image: url('../assets/img/hero.jpg');
    height: 784px;
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: flex-end;
    padding-right: 80px;
    &-img {
      max-width: 100%;
    }
    &-info{
      background: #fff;
      max-width: 630px;
      padding: 50px 55px;
      height: 444px;
      display: flex;
      flex-direction: column;
      justify-content: space-between; 
      &__title {
        font-family: 'Clash Display', sans-serif; 
        font-weight: 400;
        line-height: 1.5;
        margin: 0 0 20px 0;
      }
      &__description{
        color: #5b5676;
      }
      &-link {
        color: #2a254b;
        text-decoration: none;
        &:hover {
          text-decoration: underline;
        }
      }
    }
  }
</style>