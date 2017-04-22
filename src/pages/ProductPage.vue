<template lang="pug">
div#product-page
  p product
  
</template>

<style lang="stylus" scoped>
#product-page
  display flex
  flex-basis 100%
  flex-wrap wrap
  padding-top 3em
  padding-left 3em

</style>


<script>
import { mapGetters } from 'vuex'

export default {
  name: 'ProductPage',
  components: {

  },
  computed: {
    ...mapGetters([
      'product',
    ])
  },
  data(){
    return {

    }
  },
  created(){
    
  }
}
</script>
