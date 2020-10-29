<template>
  <div class="user-list">
    <div class="user-list__item user" v-for="(user, index) in users" :key="index">
      <div class="user__name">{{user.name}}</div>
      <div class="user__age">{{user.age}}</div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'userList',
    data() {
      return {
        users: [
          {age: 21,name: 'Andrew'},
          {age: 21,name: 'Ksks'},
          {age: 34,name: 'Yuliya'}
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
.user-list{ 
  &__item {
    margin: 20px 0;
    display: flex;
    align-items: center;
    justify-content: space-between;
  }
}
.user {
  &__age {
    font-size: 20px;
  }
  &__name {
    font-size: 25px;
  }
}

</style>