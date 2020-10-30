<template>
  <div class="cart">
    Cart
    <CartItem v-for="(item, index) in cartItems" :key="index" :num="item.num"/>
  </div>
</template>

<script>
  import CartItem from './CartItem';
  export default {
    name: 'cart',
    data() {
      return {
        cartItems: [
          {num: 1},
          {num: 2},
          {num: 3},
          {num: 4},

        ]
      }
    },
    components: {
      CartItem
    }
  }
</script>

<style lang="scss" scoped>
.cart {
  padding: 30px;
  background-color: #bbb;
}

</style>