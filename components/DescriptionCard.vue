<template>
   <div class="wrapper">
     <div class="upper-wrapper">
       <div v-if="extraDescription" class="extra-description">

       </div>
       <div class="title">
         {{item.title}}
       </div>
       <div class="description">
         {{item.description}}
       </div>
     </div>
     <BrandButton text="SHOP NOW"> </BrandButton>
     <div class="dots">
       <span class="full-dot"></span>
       <span class="empty-dot"></span>
       <span class="empty-dot"></span>
     </div>
   </div>
</template>

<script>
export default {
  name: "DescriptionCard.vue",
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    }
  },
  data() {
    return {
      item: {
        title: 'The new 2021 collection',
        description: 'Known as "the miracle plant", Aloe Vera helps to nourish, moisturize and keep the hair looking smooth. Let your hair be flexible and fresh.'
      },
    }
  }
}
</script>

<style scoped>

.wrapper {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.upper-wrapper {
  display: flex;
  flex-direction: column;

}

.title {
  margin: 48px 16px 18px 16px;
  font-weight: 700;
  font-size: 24px;
  line-height: 32px;
  color: #2A2A48;

}

.description {
  font-weight: 400;
  font-size: 16px;
  line-height: 24px;
  color: #485363;
  margin: 0 16px;
}

.empty-dot {
  height: 5px;
  width: 5px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
}

.full-dot {
  height: 8px;
  width: 8px;
  background: #505357;
  border-radius: 50%;
  display: inline-block;
}
</style>
