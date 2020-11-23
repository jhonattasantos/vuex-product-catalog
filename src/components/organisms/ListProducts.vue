<template>
    <div>
        <title-atom :tag="'h1'" :content="'Produtos'" />
        <div class="card-group">
            <template v-for="p of products">                
               <card-product :product="p" />
            </template>
        </div>
    </div>
</template>

<script>
import TitleAtom from '@/components/atoms/TitleAtom.vue'
import CardProduct from '@/components/molecules/CardProduct.vue'
export default {
  components: { TitleAtom, CardProduct },
  name: 'ListProductsOrganism',
  computed: {
    products(){
      return this.$store.state.products
    }
  }
}
</script>

<style scoped>
.card-group {
    display: flex;
    flex-wrap: wrap;
}
</style>
