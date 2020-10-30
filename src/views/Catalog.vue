<template>
  <div class="catalog">
    <h1>This is catalog page</h1>
    <catalog-list/>
  </div>
</template>

<script>
import CatalogList from '../components/CatalogList';
export default {
  name: 'Catalog',
  components: {
    CatalogList
  }
}
</script>
