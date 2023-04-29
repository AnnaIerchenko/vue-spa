<script setup>
  import {ref} from 'vue'
  const aboutBrands = [
    {
      img: '/svg/Delivery.svg',
      title: 'Next day as standard',
      description: ' Order before 3pm and get your order the next day as standard'
    },
    {
      img: '/svg/Checkmark--outline.svg',
      title: 'Made by true artisans',
      description: 'Handmade crafted goods made with real passion and craftmanship'
    },
    {
      img: '/svg/Purchase.svg',
      title: 'Unbeatable prices',
      description: 'For our materials and quality you won’t find better prices anywhere'
    },
    {
      img: '/svg/Sprout.svg',
      title: 'Recycled packaging',
      description: 'We use 100% recycled to ensure our footprint is more manageable'
    },
  ]

</script>

<template>
  <div class="about-brand">
    <h3 class="about-brand__title">
      What makes our brand different
    </h3>
    <div class="about-brand-elements">
      <div
        class="about-brand-element"
        v-for="(element, i ) of aboutBrands"
        :key="i"
      >
        <img 
          :src="element.img" 
          :alt="element.title"
          class="about-brand-element__img"
          >
        <h4 class="about-brand-element__title">
          {{element.title}}
        </h4>
        <span class="about-brand-element__description">
        {{ element.description }}
        </span>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.about-brand {
  padding: 80px 80px 130px 80px;
  margin-bottom: 50px;

  @media screen and (max-width: 767px){
    padding: 48px 24px;
    margin-top: 110px;
  }
  &__title{
    text-align: center;
    font-size: 24px;
    color: #2a254b;
    margin: 0 0 84px 0;
    @media screen and (max-width: 767px){
      text-align: left;
      font-size: 20px;
      margin-bottom: 3px;
    }
  }
  &-elements {
    display: grid;
    grid-template-columns: repeat(4, 210px);
    justify-content: space-between;
    @media screen and (max-width: 1024px){
      grid-template-columns: repeat( 2, 1fr);
      gap: 40px 20px;
    }
    @media screen and (max-width: 767px){
      grid-template-columns: 1fr;
    }
  }
  &-element{
    color: #2a254b;
    background: #f3efef;
    padding: 40px;
    @media screen and (max-width: 767px){
      padding: 16px 24px;
    }
    &__img {
      display: block;
      margin-bottom: 12px;
    }
    &__title{
      margin: 0 0 12px 0;
      font-size: 20px;
    }
    &__description{
      font-size: 16px;
      line-height: 1.5;
    }
  }
}
</style>