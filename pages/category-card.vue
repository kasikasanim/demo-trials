<template>
   <div class="card-container">
     <div class="card-wrapper" v-for="category in categories" :key="category.id">
       <div class="foreground-container">
         <div class="category-title">
           {{category.title}}
         </div>
         <div class="category-description">
           {{category.description}}
         </div>
         <div class="category-button" >
           <BrandButton text="BROWSE" />
         </div>
       </div>
     </div>
     <Newsletter/>
   </div>
</template>

<script>
import BrandButton from "~/components/BrandButton";
import Newsletter from "@/components/Newsletter";
export default {
  name: "category-card.vue",
  components: {
    BrandButton,
    Newsletter
  },
  data() {
    return {
      categories: [
        {id: '1', title: 'Personal Care', description: 'Lorem ipsum dolor sit amet consectetu elit aliquam'},
        {id: '2', title: 'Skin Care', description: 'Lorem ipsum dolor sit amet consectetu elit aliquam'},
        {id: '3', title: 'Make - Up', description: 'Lorem ipsum dolor sit amet consectetu elit aliquam'},
        {id: '4', title: 'Mother & Baby', description: 'Lorem ipsum dolor sit amet consectetu elit aliquam'}
      ]
    }
  }

}

</script>

<style scoped>

/deep/ .button {
  background: #0099A8 !important;
  padding: 0.75rem;
}

.card-wrapper {
  display: flex;
  justify-content: center;
  background-image: url("../static/Banner.png");
  background-position: center;
  background-size: cover;
  margin-bottom: 1.25rem;
}
.foreground-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 2.5rem;
  background: white;
  opacity: 0.9;
  max-width: 75%;
  max-height: 75%;
  margin: 1.25rem;
}

.category-title {
  font-style: normal;
  font-weight: 700;
  font-size: 20px;
  line-height: 24px;
  margin-bottom: 0.75rem;

}

.category-description {
  font-style: normal;
  font-weight: 400;
  font-size: 14px;
  line-height: 24px;
}

</style>
