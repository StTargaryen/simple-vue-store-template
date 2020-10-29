<template>
  <div class="catalog">
    <h1>This is catalog page</h1>
    <userList/>
  </div>
</template>

<script>
import userList from '../components/userList'
export default {
  name: 'Catalog',
  components: {
    userList
  }
}
</script>
