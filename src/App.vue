<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Catalog</router-link>
      <router-link to="/cart">to Cart</router-link>
    </div>
    <router-view/>
  </div>
</template>

<script>
export default {
}
</script>

<style lang="scss">
* {
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin: 0 auto;
  max-width: 900px;
}

#nav {
  padding: 30px;
  display: flex;
  justify-content: center;

  a {
    font-weight: bold;
    color: #2c3e50;
    padding: 10px 25px;
    margin: 0 20px;
    border: 2px solid #ccc;
    border-radius: 20px;
    text-decoration: none;
    box-shadow: 2px 2px #ccc;
    transition: all .3s ease-in-out;

    &:hover {
      background-color: #ccc;
    }

    &.router-link-exact-active {
      color: white;
      background: #42b983;
      border-color: #42b983;
      box-shadow: none;
    }
  }
}

.btn {
  background: transparent;
  color: inherit;
  font-size: inherit;
  border: 0;
  outline: 0;
}
</style>
