<template>
  <div class="hero">
    <div class="hero-upper">
      <div class="ellipse-1">
       <img src="../static/ellipse-1.png">
      </div>
      <div class="ellipse-2">
        <img src="../static/ellipse-2.png">
      </div>
      <div class="bottle-1">
        <img src="../static/bottle-1.png">
      </div>
      <div class="bottle-2">
        <img src="../static/bottle-2.png">
      </div>
      <div class="bottle-3">
        <img src="../static/bottle-3.png">
      </div>
      <div class="leaves">
        <img src="../static/leaves.png">
      </div>
    </div>
    <div class="hero-lower">
      <DescriptionCard />
    </div>
  </div>
</template>

<script>
import DescriptionCard from "@/components/DescriptionCard";
export default {
  name: "Hero.vue",
  components: {
    DescriptionCard
  }
}
</script>

<style scoped>
 /** 500pxten sonra media query ile flexi rowa çevir**/
 /** 2li kartlarda wrap yukarı dönünce margini bu şekilde koy https://developer.mozilla.org/en-US/docs/Web/CSS/:nth-of-type **/

 /deep/ .button {
   min-height: 32px;
 }
.hero {
  padding: 12px;
  background: linear-gradient(163.21deg, #F2F0FF 9.01%, rgba(251, 251, 255, 0.77) 26.47%, rgba(255, 255, 255, 0.72) 52.19%, #F2F0FF 67.81%), #F2F0FF;
}

.hero-upper {
  position: relative;
  height: 300px;
}

.ellipse-1 {
  position: absolute;
  left: 60px;
  right: 8.22%;
  top: 15px;
  bottom: 0%;

}

.ellipse-2 {
  position: absolute;
  left: 90px;
  right: 0%;
  top: 0%;
  bottom: 5.52%;
}

.bottle-1 {
  position: absolute;
  width: 66px;
  height: 211px;
  left: 250px;
  top: 37px;

}

.bottle-2 {
  position: absolute;
  width: 166px;
  height: 166px;
  left: 63px;
  top: 97px;
  z-index: 95;

}

.bottle-3  {
  position: absolute;
  width: 218px;
  height: 217px;
  left: 95px;
  top: 31px;
  z-index: 100;

}

.leaves {
  position: absolute;
  width: 216px;
  height: 203px;
  left: 10px;
  top: 27px;
}
</style>
