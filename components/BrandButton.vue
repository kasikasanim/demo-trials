<template>
  <div class="button-container">
    <button class="button" >
      {{ text }}
    </button>
  </div>
</template>

<script>
export default {
  name: "BrandButton.vue",
  props: {
    text: {
      type: String,
      required: true
    },

  },

}
</script>

<style scoped>

.button {
  background: #FF27AD;
  border-radius: 4px;
  color: white;
  width: 100%;
  border: none;
  margin-top: 16px;
  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  line-height: 16px;

}

.button-container {
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: 1rem;
}
</style>
