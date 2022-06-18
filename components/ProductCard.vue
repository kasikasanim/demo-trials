<template>
 <div class="product-card-container">
   <div class="product-card-wrapper" v-for="item in items">
     <div class="img-wrapper">
       <img :src=item.thumbnail :alt=item.description class="image-container">
     </div>
     <div class="price-description-wrapper">
       <div class="price">
         {{item.price + ' TL'}}
       </div>
       <div class="description">
         {{item.description}}
       </div>
     </div>
     <div class="add-button-wrapper">
       <button class="add-button">
         <img src="../static/add-to-basket-icon.png" alt="add-to-basket">
         ADD
       </button>
     </div>
   </div>


 </div>
</template>

<script>
import DescriptionCard from '@/components/DescriptionCard'
export default {
  name: "ProductCard.vue",
  components: {
    DescriptionCard
  },
  props: {
    items: {
      type: Array,
      required: true,
    }
  }



}
</script>

<style scoped>

.product-card-container {
  display: flex;
  flex-wrap: wrap;
}
.product-card-wrapper {
  padding: 2.5rem;
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  background-color: rgba(236, 236, 236, 0.16);
  max-width: 15rem;
  justify-content: flex-start;
}

.image-container {
  max-width: 100%;
  max-height: 8rem;
}

.img-wrapper {
  max-height: 50%;
}

.price {
  margin: 8px 0;
  font-style: normal;
  font-weight: 700;
  font-size: 16px;
  line-height: 16px;
}

.description {
  margin: 16px 0;
  font-style: normal;
  font-size: 14px;
  line-height: 24px;
}

.add-button-wrapper {
  width: 100%;
  display: flex;
  justify-content: center;
  margin-top: 1rem;

}

.add-button {
  width: 12rem;
  background: #FF27AD;
  border-radius: 4px;
  padding: 0.25rem;
  color: white;
  text-align: center;
  border: none;
  font-weight: 700;
}


</style>
