<template>
  <div class="cart-item">
    <div class="cart-item__wrapper">
      <img class="cart-item__image" :src="item.url" alt="">
      <div class="cart-item__title">{{item.title}}</div>
      <button @click="removeFromCart" class="btn cart-item__button">Remove</button>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'cart-itme',
    props: {
      item: Object
    },
    methods: {
      removeFromCart() {
        this.$emit('removeItem', this.item)
      }
    }
  }
</script>

<style lang="scss" scoped>
.cart-item {
  background-color: #ccc; margin: 20px 0;
  padding: 5px;

  &__wrapper {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  &__image {
    widows: 100%;
    max-height: 100px;
  }
  &__title {
    flex: 1;
    font-size: 20px;
    margin-left: 20px;
  }
  &__button {
    color: #fff;
    font-weight: bold;
    background: #42b983;
    padding: 10px 25px;
    border: 2px solid #ccc;
    border-radius: 20px;
    box-shadow: 2px 2px #ccc;
    transition: all .3s ease-in-out;
    cursor: pointer;
    
    &:hover {
      background-color: #ccc;
      border-color: #42b983;
      color: #42b983;

    }
  }
}
</style>