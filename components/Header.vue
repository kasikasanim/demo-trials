<template>
  <div class="header">
    <div class="header-up">
      <div class="header-up-left">
        <div class="header-headings">
          <div class="stores-icon">
            <img src="../static/stores.png" width="18px" alt="stores-icon">
          </div>
          <div class="text">Stores</div>
        </div>
        <div class="header-headings">
          <div class="catalog-icon">
            <img src="../static/katalog.png" width="18px" alt="catalog-icon">
          </div>
          <div class="text">Catalog</div>
        </div>
      </div>
      <div class="header-up-right">
        <div class="phone-icon">
          <img src="../static/phone.png" width="18px" alt="phone-icon">
        </div>
      </div>
      <div v-if="mobile" class="header-up-middle">
        Watsons Beauty and Personal Care Awards Nominees!
      </div>
      <div v-if="mobile" class="header-up-right">
        Call us:(+90) 850 123 45 67
      </div>
    </div>
    <div class="header-bottom">
      <div class="bottom-logo">
        <img src="../static/watsons-logo.png" alt="watsong-logo">
      </div>
      <div class="bottom-navigation">
        <div class="nav-icons">
          <img src="../static/search-icon.png" alt="search-icon" width="18px">
        </div>
        <div class="nav-icons">
          <img src="../static/basket-icon.png" alt="basket-icon">
        </div>
        <div class="nav-icons">
          ///
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Slide , Menu} from 'vue-burger-menu'
export default {
  name: 'Header',
  components: {
    Slide,
    Menu
  },
  data() {
    return {
      mobile: false
    }
  },
  methods: {
    /**
     * method ne iş yapıyor, extra iş var mı? dökümantasyonu yap. (/** dan sonra entera bas)
     * @param name
     * @param age
     */
    test(name, age) {

    }
  }
}


</script>

<style>

.header {
  background-color: #505357;
}

.header-headings {
  display: flex;
}

.header-up {
  display: flex;
  justify-content: space-between;
}


.header-up-left {
  display: flex;
  flex-direction: row;
  width: 50%;
  justify-content: space-evenly;
  align-items: center;

}

.header-up-right {
  margin-right: 16px;
  margin-bottom: 9px;
}

.stores-icon {
  margin: 0 8px 0 16px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.catalog-icon {
  margin: 0 8px 0 16px;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

.text {
  color: white;
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 24px;
}

.bm-burger-button {
  cursor: pointer;
  height: 30px;
   left: 20px;
  position: absolute;
  top: 36px;
  width: 36px;
}

.header-bottom {
  background: white;
  display: flex;
  justify-content: space-between;
}

.bottom-logo {
  width: 40%;
  margin: 16px;
}
.bottom-navigation {
  display: flex;
  width: 60%;
  justify-content: space-evenly;
  margin: 16px;
}

.nav-icons {
  margin-left: 18px;
}
</style>
