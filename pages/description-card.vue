<template>
  <DescriptionCard :title="title" :description="description"></DescriptionCard>
</template>

<script>
import DescriptionCard from "@/components/DescriptionCard";
export default {
  name: "description-card.vue",
  data () {
    return {
      title: 'The new 2021 collection',
      description: 'Known as "the miracle plant", Aloe Vera helps to nourish, moisturize and keep the hair looking smooth. Let your hair be flexible and fresh.',
    }
  },
  components: {
    DescriptionCard
  }
}
</script>

<style scoped>

</style>
