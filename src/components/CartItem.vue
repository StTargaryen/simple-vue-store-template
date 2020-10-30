<template>
  <div class="cart-item">
    Cart item № {{num}}
  </div>
</template>

<script>
  export default {
    name: 'cart-itme',
    props: ['num']
  }
</script>

<style lang="scss" scoped>
.cart-item {background-color: #ccc; margin: 20px 0;}
</style>