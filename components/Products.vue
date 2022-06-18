<template>
<div class="product-wrapper">
  <div class="heading-wrapper">
    <div> DIVIDER </div>
    <div> Featured Products </div>
    <div> DIVIDER </div>
  </div>

  <div class="product-card">
     <ProductCard :items="products" ></ProductCard>
  </div>
</div>
</template>

<script>
import ProductCard from '@/components/ProductCard'
export default {
  name: "Products.vue",
  components: {ProductCard},
  data() {
    return {
      products: [],
    }
  },


   methods: {
   async getData() {
     const response = await fetch('https://dummyjson.com/products?limit=10')
     const data = await response.json();
     this.products = data.products;
     console.log(this.products)
   },

  },
  created() {
    this.getData()
  }
}
</script>

<style scoped>

.heading-wrapper {
  margin: 1.5rem;
}
.product-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}

.heading-wrapper {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

</style>
