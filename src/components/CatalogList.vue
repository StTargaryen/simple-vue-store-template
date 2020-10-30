<template>
  <div class="catalog-list">
    Catalog List
    <catalog-item/>
  </div>
</template>

<script>
import CatalogItem from './CatalogItem';
  export default {
    name: 'catalog-list',
    components: {
      CatalogItem
    }
  }
</script>

<style lang="scss" scoped>
.catalog-list {
  padding: 30px;
  background-color: #bbb;
}

</style>