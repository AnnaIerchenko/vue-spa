<script setup>
   import uiButton from "@/components/UI/Button.vue"
   const props = defineProps({
    bgInput: {
      type: String,
      required: false
    },
    colorButton: {
      type: String,
      required: false
    },
    colorText: {
      type: String,
      required: false
    },
   })
</script>

<template>
  <form class="subscribe-form">
    <input 
      type="text" 
      placeholder="your@email.com" 
      class="input-text suscribe-form__input"
      :style="{backgroundColor: bgInput, color: colorText}"

      >
    <ui-button :color="colorButton || 'primary'">Sign Up</ui-button>
  </form>

</template>

<style lang="scss" scoped>
  form{
    display: flex;
  }
  @media screen and (max-width: 767px){
    .input-text {
      width: 80%;
    }
  }
  // .subscribe-form{
  //   display: flex;
  //   &__input{
  //     flex-grow: 1;
  //   }
  // }
</style>