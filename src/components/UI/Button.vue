<script setup>
  const props = defineProps({
    background: {
      type: String,
      required: false
    },
    type: {
      type: String,
      default: 'button'
    },
    to: {
      type: String,
      required: false
    },
    color: {
      type: String,
      default: 'primary'
    },
    mobileFullWidth: {
      type: Boolean,
      default: false
    }
  })
</script>


<template>
  <button 
    v-if="type === 'button'"
    class="btn" 
    :class="['btn', 
    {
      'btn--primary': color === 'primary',
      'btn--secondary': color === 'secondary',
      'btn--lightgray': color === 'lightgray',
      'btn--fullwidth' : mobileFullWidth
    }]">
    <slot />
  </button>
  <router-link 
    v-else class="btn"
    :to="to"
    :class="['btn', 
    {
      'btn--primary': color === 'primary',
      'btn--secondary': color === 'secondary',
      'btn--lightgray': color === 'lightgray',
      'btn--fullwidth' : mobileFullWidth
    }]"
    >
    <slot />
  </router-link>
</template>

<style lang="scss" scoped>
.btn {
  padding: 0 32px;
  display: flex;
  align-items: center;
  justify-content: center;
  border: none;
  font-size: 16px;
  height: 56px;
  cursor: pointer;
  text-decoration: none;
  white-space: nowrap;
  &:hover {
    opacity: 0.8;
  }
  &--primary{
    background: #2a254b;
    color: #fff;
  }
  &--secondary {
    background: rgba(249, 249, 249, 0.15);
    color: #fff;
  }
  &--lightgray{
    background: #f9f9f9;
    color: #2a254b;
  }
  &--white{
    background: #fff;
    color: #2a254b;
  }
  &--fullwidth{
    @media screen and (max-width: 767px) {
      width: 100%;
      padding: 32px;
    }
  }
}
</style>