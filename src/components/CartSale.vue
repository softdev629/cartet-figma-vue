<template>
  <div class="container">
    <MainHeader />
    <div class="container-section">
      <SideBarDesktop type="3" />
      <CartSaleItems />
      <CartSold />
    </div>
  </div>
</template>

<script>
import MainHeader from "./cart/MainHeader.vue";
import CartSaleItems from "./cart/desktop/CartSaleItems.vue";
import CartSold from "./cart/desktop/CartSold.vue";
import SideBarDesktop from "./cart/desktop/SideBarDesktop.vue";
import CartPageMobile from "./cart/mobile/CartPageMobile.vue";
export default {
  components: {
    MainHeader,
    SideBarDesktop,
    CartSaleItems,
    CartPageMobile,
    CartSold,
  },
  name: "CartSale",
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
    getDeviceType() {},
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
