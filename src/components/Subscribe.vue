<script setup>
  import SubscribeForm from "@/components/SubscribeForm.vue";
</script>

<template>
  <div class="subscribe">
    <div class="subscribe-content">
      <h3 class="subscribe-title">Join the club and get benefits</h3>
      <span class="subscribe-description">
        Sign up for our news letter aand receive exclusive offers sales, pop up stories and more
      </span>
      <div class="subscribe-checks">
        <div class="subscribe-check">
          <img src="/svg/check.svg" alt="check" class="subscribe-check__icon">
          <span class="subscribe-checks__name">Exclusive offer</span>
        </div>
        <div class="subscribe-check">
          <img src="/svg/check.svg" alt="check" class="subscribe-check__icon">
          <span class="subscribe-checks__name">Free events</span>
        </div>
        <div class="subscribe-check">
          <img src="/svg/check.svg" alt="check" class="subscribe-check__icon">
          <span class="subscribe-checks__name">Large discout</span>
        </div>
      </div>
      <SubscribeForm />
      <!-- <form class="suscribe-form">
        <input type="text" placeholder="your@email.com" class="input-text suscribe-form__input">
        <ui-button>Sign Up</ui-button>
      </form> -->
    </div>
  </div>
</template>


<style lang="scss" scoped>
  .subscribe {
    background-image: url("../assets/img/hero.jpg");
    background-size: cover;
    padding: 97px 0 86px 0;
    min-height: 444px;
    @media screen and (max-width: 767px){
      padding: 74px;
      margin: 0 -34px;
      margin-bottom: 30px;
    }
    &-content{
      max-width: 500px;
      margin: auto;
      text-align: center;
      // color: #fff;
      // background-color: #fff;
      padding: 40px;
      @media screen and (max-width: 767px){
        text-align: left;
      }
    }
    &-title {
      display: block;
      margin: 0 0 12px 0;
      font-size: 12px;
      font-weight: 400px;
      font-family: 'Clash Display', sans-serif;
    }
    &-description{
      display: block;
      font-size: 18px;
      margin-bottom: 30px;
      @media screen and (max-width: 767px){
        font-size: 14px;
        margin-bottom: 20px;
      }
    }
    &-checks{
      display: flex;
      justify-content: center;
      margin-bottom: 40px;
      @media screen and (max-width: 767px){
        display: block;
  
      }
    }
    &-check{
      display: flex;
      align-items: center;
      &:nth-child(2){
        margin: 0 36px;
      }
      @media screen and (max-width: 767px){
        margin: 0;
       
      }
      &__icon{
        margin-right: 5px;
      }
    }
  
    form {
      display: flex;
      @media screen and (max-width: 767px){
        display: block;
        margin: 0 10px;
      }
    }
  }
</style>