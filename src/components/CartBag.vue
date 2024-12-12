<template>
  <!-- Wrap the icon and the cart in a container that is position: relative -->
  <div class="icon" style="position: relative;">
    <div class="carticon" @click="showCart = !showCart">
      <div class="count">{{ cartLength }}</div>
      <img src="../assets/graphics/bag.svg" alt="Carticon" />
    </div>

    <!-- Place the Cart component absolutely inside this container -->
    <div v-if="showCart" class="cart-container">
      <Cart />
    </div>
  </div>
</template>

<script>
import Cart from "./Cart";
export default {
  name: "CartBag",
  components: { Cart },
  data() {
    return { showCart: false };
  },
  computed: {
    cartLength() {
      let total = 0;
      this.$store.state.cart.forEach(item => {
        total += item.quantity;
      });
      return total;
    }
  }
};
</script>

<style lang="scss" scoped>
.icon {
  position: relative; /* Ensure the cart is positioned relative to this container */
  padding-left: 300px; /* You can adjust or remove this padding as needed */
}

/* This container will appear right below the carticon */
.cart-container {
  position: absolute;
  top: 100%;   /* Position it directly below the .carticon */
  right: 0;   /* Align it to the right edge (or left:0 if you want it aligned left) */
}
.carticon {
  background: black;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 1.2rem;
  height: 1.2rem;
  padding: 1.6rem;
  border-radius: 100%;
  float: right;
  margin-top: -150px; /* You may need to adjust or remove these margins to get desired placement */
  margin-right: 30px;
  cursor: pointer;

  .count {
    position: absolute;
    width: 2rem;
    height: 2rem;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 100%;
    background: orange;
    font-size: 1rem;
    font-weight: 700;
    z-index: 2;
    margin-left: 50px;
    margin-top: 35px;
  }
}
</style>
