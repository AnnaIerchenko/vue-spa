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
</script>

<template>
  <header class="header">
    <div class="header-top">
      <div class="header-top-search">
        <img src="/svg/Search.svg" alt="search">
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
  </header>
</template>

<style lang="scss" scoped>
  .header {
    height: 132px;
    background: #fff;
    margin: 0 28px;
 
    &-top{
      display: flex;
      justify-content: space-between;
      height: 70px;
      align-items: center;
      border-bottom: 1px solid rgba(0, 0, 0, .1);

      &-right {
        display: flex;
        align-items: center;
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
      &:hover{
        text-decoration: underline;
      }
    }
    &-menu {
      height: 62px;
      display: flex;
      justify-content: center;
      align-items: center;
      &__link{
        margin: 0 22px;
        color: #726e8d;
        text-decoration: none;
        &:hover {
          text-decoration: underline;
        }
      }
    }
  }
</style>