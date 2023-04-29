<script setup>
  import {ref} from 'vue'
  const menu = [
   { 
    name: 'Plant pots',
    path: '/plant'
    },
   { 
    name: 'Ceramics',
    path: '/ceramics'
    },
   { 
    name: 'Tables',
    path: '/tables'
    },
  ]
  const isOpenMobileMenu = ref(false)
</script>

<template>
  <header class="header">
    <div class="header-top">
      <div class="header-top-left">
        <div class="header-top-search">
          <img src="/svg/Search.svg" alt="search" class="header-top__icon">
        </div>
        <div class="header-top-mobile-menu" @click="isOpenMobileMenu = !isOpenMobileMenu">
          <img src="/svg/menu.svg" alt="menu" class="header-top">
        </div>
      </div>
      <router-link to="/" class="header-logo">Avion</router-link>
      <div class="header-top-right">
        <div class="header-top-right__cart">
          <router-link to="/cart">
          <img src="/svg/Shopping--cart.svg" alt="cart">
          </router-link>
        </div>
        <div class="header-top-user--avatar">
          <router-link to="/user">
            <img src="/svg/User--avatar.svg" alt="user">
          </router-link>
        </div>
      </div>
    </div>
    <div class="header-menu">
      <router-link
        class="header-menu__link"
        :to="element.path" 
        v-for="(element, i) of menu"
        :key="i"
        >{{ element.name }}</router-link>
    </div>
    <div class="header-menu-mobile" v-if="isOpenMobileMenu">
      <router-link
        class="header-menu-mobile__link"
        :to="element.path" 
        v-for="(element, i) of menu"
        :key="i"
        >{{ element.name }}</router-link>
  </div>
  </header>
</template>

<style lang="scss" scoped>
  .header {
    height: 132px;
    background: #fff;
    position: relative;
    margin: 0 28px;
    @media screen and (max-width: 767px){
      height: auto;
    }
    &-top{
      display: flex;
      justify-content: space-between;
      height: 70px;
      align-items: center;
      border-bottom: 1px solid rgba(0, 0, 0, .1);
      margin: 0 2px;
      @media screen and (max-width: 767px){
        margin: 0;
        bottom: none;
        height: auto;
        padding: 20px 0;
       
      }
      &__icon {
        display: block;
      }
      &-left {
        display: flex;
        align-items: center;
        justify-content: baseline;
        @media screen and (max-width: 767px){
          order: 2;
        }
      }
      &-mobile-menu {
        display: none;
        margin-left: 15px;
        @media screen and (max-width: 767px){
          display: block;
        }
      }
      &-right {
        display: flex;
        align-items: center;
        justify-content: flex-end;
        @media screen and (max-width: 767px){
          display: none;
        }
        &__cart{
          margin-right: 16px;
        }
      }
    }
    &-logo{
      color: #22202e;
      font-size: 24px;
      text-decoration: none;
      font-family: 'Clash Display', sans-serif;
      text-align: center;
      @media screen and (max-width: 767px){
        order: 1;
      }
      &:hover{
        text-decoration: underline;
      }
    }
    &-menu {
      height: 62px;
      display: flex;
      justify-content: center;
      align-items: center;
      @media screen and (max-width: 767px){
        display: none;
      
      }
      &__link{
        margin: 0 22px;
        color: #726e8d;
        text-decoration: none;
        &:hover {
          text-decoration: underline;
        }
      }
      &-mobile {
        position: absolute;
        background: #fff;
        top: 60px;
        padding: 10px;
        border: 1px solid #000;
        width: 100%;
        &__link{
          display: block;
          margin: 22px;
          color: #726e8d;
          text-decoration: none;
          &:last-child{
            margin-bottom: 0;
          }
          &:hover {
            text-decoration: underline;
          }
        }
      }
    }
  }
</style>