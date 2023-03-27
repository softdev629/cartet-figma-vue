<template>
  <div class="resell-cart__container">
    <div class="top-app__bar">
      <span>&lt; Your Carts</span>
      <span> &lt; 1st Grader Grils</span>
      <span class="active"> &lt; Resale Items</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "ResellPageMobile",
};
</script>

<style scoped>
.resell-cart__container {
  flex: 1;
}

.top-app__bar {
  background-color: #0b2560;
  padding: 15px 20px;
  color: white;
  font-size: 14px;
  font-family: "Poppins";
  line-height: 17px;
}

.top-app__bar .active {
  font-weight: 600;
}
</style>
