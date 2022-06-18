<template>
  <div id="app">
    <Header />
    <Hero />
    <Products />
  </div>

</template>

<script>
import Header from '@/components/Header'
import Hero from '@/components/Hero'
import Products from "@/components/Products";
export default {
  name: 'IndexPage',
  components: {
    Header,
    Hero,
    Products
  }
}


</script>

