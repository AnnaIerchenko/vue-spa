<script setup>
  import SubscribeForm from "@/components/SubscribeForm.vue";
</script>

<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-top">
        <div class="footer-menu">
          <div class="footer-menu-column">
            <span class="footer-menu__title">Menu</span>
            <router-link to="/" class="footer-menu__link">New Arrivals</router-link>
            <router-link to="/" class="footer-menu__link">Best sellers</router-link>
            <router-link to="/" class="footer-menu__link">Recently viewed</router-link>
            <router-link to="/" class="footer-menu__link">Popular this week</router-link>
            <router-link to="/" class="footer-menu__link">All products</router-link>
          </div>
          <div class="footer-menu-column">
            <span class="footer-menu__title">Categories</span>
            <router-link to="/" class="footer-menu__link">Crockery</router-link>
            <router-link to="/" class="footer-menu__link">Furniture</router-link>
            <router-link to="/" class="footer-menu__link">Homeware</router-link>
            <router-link to="/" class="footer-menu__link">Plant pots</router-link>
            <router-link to="/" class="footer-menu__link">Chairs</router-link>
            <router-link to="/" class="footer-menu__link">Crockery</router-link>
          </div>
          <div class="footer-menu-column">
            <span class="footer-menu__title">Our Company</span>
            <router-link to="/" class="footer-menu__link">About Us</router-link>
            <router-link to="/" class="footer-menu__link">Vacancies</router-link>
            <router-link to="/" class="footer-menu__link">Contacts</router-link>
            <router-link to="/" class="footer-menu__link">Privacy</router-link>
            <router-link to="/" class="footer-menu__link">Returns policy</router-link>
          </div>
        </div>
        <div class="footer-subscribe">
           <SubscribeForm 
            colorButton="white" 
            bgInput="rgba(255, 255, 255, 0.15)"
            colorText= "#fff"
            />
        </div>
      </div>
      <div class="footer-bottom">
        <span class="footer-bottom__copyright">
          Copyright 2023 Avion LTD
        </span>
        <div class="footer-bottom-social">
          <a href="#" class="footer-bottom-social__link">
            <img src="/svg/linkedin.svg" alt="">
          </a>
          <a href="#" class="footer-bottom-social__link">
            <img src="/svg/facebook.svg" alt="">
          </a>
          <a href="#" class="footer-bottom-social__link">
            <img src="/svg/instagram.svg" alt="">
          </a>
          <a href="#" class="footer-bottom-social__link">
            <img src="/svg/skype.svg" alt="">
          </a>
          <a href="#" class="footer-bottom-social__link">
            <img src="/svg/twitter.svg" alt="">
          </a>
          <a href="#" class="footer-bottom-social__link">
            <img src="/svg/pinterest.svg" alt="">
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
  .footer{
    background: #2a254b;
    color: #fff;
    &-content{
      padding: 50px 82px 25px 82px;
   
    }
    &-top{
      display: grid;
      grid-template-columns: 540px 1fr;
      column-gap: 110px;
      border-bottom: 1px solid #4e4d93;
    
    }
    &-menu{
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      margin-bottom: 22px;
      &__title{
        font-family: 'Clash Display', sans-serif; 
        display: block;
        margin-bottom: 12px;
      }
      &__link{
        display: block;
        color: #fff;
        font-size: 14px;
        text-decoration: none;
        margin-bottom: 12px;
        &:last-child{
          margin-bottom: 0;
        }
        &:hover{
          text-decoration: underline;
        }
      }
    }
    &-bottom{
      padding-top: 22px;
      display: flex;
      justify-content: space-between;
      &__copyright{
        font-size: 14px;
      }
      &-social{
        display: flex;
        align-items: center;
        &__link{
          margin: 0 12px;
          &:hover{
            opacity: 0.8;
          }
        }
      }
    }
  }
</style>