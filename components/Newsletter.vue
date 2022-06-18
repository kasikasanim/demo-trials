<template>
 <div class="newsletter-container">
   <div class="heading-content-container">
     <div class="heading">
       Sign up to our newsletter
     </div>
     <div class="content">
       Be the first to hear about the latest offers.
     </div>
   </div>
   <div class="email-subscribe">
     <div class="email-input-container">
       <input type="text" class="email-input">
     </div>
     <div class="subscribe-button">
        <BrandButton text="SUBSCRIBE" />
     </div>
   </div>
 </div>
</template>

<script>
export default {
  name: "Newsletter.vue"
}
</script>

<style scoped>
/deep/ .button {
  background: #FF27AD !important;
  margin-top: 0;
  min-height: 3rem;
}


.email-subscribe {
  display: flex;
  align-items: center;
}

.email-input {
  min-height: 3rem;
  min-width: 220px;
}

.newsletter-container {
  background: #F2F0FF;
  padding: 1rem;
}

.heading {
  font-weight: 700;
  font-size: 1.25rem;
  line-height: 1.5rem;
  margin-bottom: 0.5rem;


}

.content {
  font-size: 14px;
  color: rgba(42, 42, 72, 0.6);
  font-size: 14px;
  line-height: 16px;
}
</style>
