<template>
  <div class="home">
    <h1>Products</h1>
    <ProductsContainer />
  </div>
</template>

<script>
// @ is an alias to /src
import ProductsContainer from '@/components/Products.vue'
export default {
  components: {
    ProductsContainer
  }
}
</script>
