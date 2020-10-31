<template>
  <div class="cart">
    Cart
    <CartItem v-for="(item, index) in cartItems" @removeItem="removeItemFromCart" :key="index" :item="item"/>
  </div>
</template>

<script>
  import CartItem from './CartItem';
  import axios from 'axios';
  export default {
    name: 'cart',
    data() {
      return {
        cartItems: [],
        url: 'http://jsonplaceholder.typicode.com/photos?_start=0&_limit=5'
      }
    },
    components: {
      CartItem
    },
    methods: {
      GetItems() {
        axios.get(this.url)
          .then(response => {
            this.cartItems = response.data;
          })
      },
      removeItemFromCart(currentItem) {
        if(this.cartItems !== {}) {
          const newArr = this.cartItems.filter(item=> item !== currentItem);
          this.cartItems = newArr;
        }
      }
    },
    mounted() {
      this.GetItems()
    }
  }
</script>

<style lang="scss" scoped>
.cart {
  padding: 30px;
  background-color: #bbb;
}

</style>