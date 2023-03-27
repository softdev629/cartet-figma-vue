<template>
  <div class="container">
    <MainHeader />
    <div v-if="deviceType === 'desktop'">
      <div class="container-section">
        <SideBarDesktop type="1" />
        <CartPage />
      </div>
    </div>
    <div v-else>
      <div class="container-mobile">
        <CartPageMobile />
      </div>
    </div>
  </div>
</template>

<script>
import MainHeader from "./cart/MainHeader.vue";
import CartPage from "./cart/desktop/CartPage.vue";
import SideBarDesktop from "./cart/desktop/SideBarDesktop.vue";
import CartPageMobile from "./cart/mobile/CartPageMobile.vue";
export default {
  components: { MainHeader, SideBarDesktop, CartPage, CartPageMobile },
  name: "IndexPage",
  data() {
    return {
      deviceType: "",
    };
  },

  mounted() {
    this.getDeviceType();
    window.addEventListener("resize", this.getDeviceType);
  },

  methods: {
    getDeviceType() {
      if (window.innerWidth <= 480) {
        this.deviceType = "mobile";
      } else {
        this.deviceType = "desktop";
      }
    },
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
}

.container-section {
  display: flex;
  justify-content: row;
}

body {
  margin: 0px;
}

.container-mobile {
  display: flex;
  justify-content: row;
}
</style>
