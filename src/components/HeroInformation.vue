<script setup>
import uiButton from '@/components/UI/Button.vue';
  const props = defineProps({
    title: {
      type: String,
      required: false
    },
    description: {
      type: String,
      required: false
    },
    link: {
      type: String,
      required: false
    },
    colorTitle: {
      type: String,
      default: ''
    },
    colorDescription: {
      type: String,
      default: '#585676'
    },
    colorLink: {
      type: String,
      required: false
    },
    background: {
      type: String,
      default: '#fff'
    },
  })
</script>

<template>
     <div 
      class="hero-info"
      :style="{backgroundColor: background}"
     >
    <div 
      class="hero-info-text"
   
      >
        <h2 
          class="hero-info__title"
          :style="{color: colorTitle}"  
        >
          {{ title }}
        </h2>
        <span 
          class="hero-info__description"
          :style="{color: colorDescription}"
          >
        {{ description }}
        </span>
      </div>
    
      <ui-button 
        :mobileFullWidth="true"
        :color="colorLink || 'secondary'"
        type="link"
        to="/"
        >
        View collection
      </ui-button>
      <img class="hero-info__image" src="../assets/img/hero.jpg" alt="hero"/>
      <!-- <a 
        :href="link" 
        class="hero-info-link"
        :style="{colorLink: colorLink}" 
      >View collection</a> -->
    </div>
</template>

<style lang="scss" scoped>
  .hero{
    &-info{
      background: #fff;
      max-width: 630px;
      padding: 50px 55px;
      min-height: 444px;
      display: flex;
      flex-direction: column;
      justify-content: space-between; 
      align-items: flex-start;
      @media screen and (max-width: 767px){
        padding: 47px 24px 32px 24px;
        min-height: 0;
      }
      &__image {
        margin-top: 32px;
      }
      &-text {
        @media screen and (max-width: 767px){
          margin-bottom: 32px;
        }
      }
      &__title {
        font-family: 'Clash Display', sans-serif; 
        font-weight: 400;
        line-height: 1.5;
        margin: 0 0 20px 0;
      }
      &__description{
        color: #5b5676;
      }
      // &-link {
      //   color: #2a254b;
      //   text-decoration: none;
      //   width: 170px;
      //   height: 54px;
      //   display: flex;
      //   align-items: center;
      //   justify-content: center;
      //   background: rgba(249, 249, 249, 0.15);
      //   cursor: pointer;
      //   &:hover {
      //     text-decoration: underline;
      //     background: rgba(249, 249, 249, 0.45);
      //   }
      // }
    }
  }
</style>