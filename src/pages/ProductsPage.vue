<template lang="pug">
div#products-page.page
  div.header
    h2.product-count {{filteredProducts.length}} products available

  div.product-list
    div.product-container(v-for="product in filteredProducts")
      product-list-item(:product="product")
</template>

<script>
import ProductListItem from 'components/ProductListItem'
import { mapGetters } from 'vuex'
 
export default {
  name: 'ProductPage',
  components: {
    'product-list-item': ProductListItem,
  },
  computed: {
    ...mapGetters([
      'products',
      'filteredProducts',
      'productFilters'
    ])
  },
}
</script>

<style lang="stylus" scoped>
#products-page
  display flex
  flex-basis 100%
  flex-wrap wrap
 
  .header
    display flex
    flex-basis 100%
    margin-bottom 20px
    align-items center

    .product-count
      font-size 20px
      color #1f2532
      font-weight normal  

    .product-filter
      margin-left auto

  .product-list
    display flex
    flex-basis 100%
    flex-wrap wrap
    zoom .5

    .product-container
      display flex
      flex-basis 100%
      margin-bottom 15px

</style>
