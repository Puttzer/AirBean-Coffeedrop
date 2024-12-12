<template>
  <div class="cartview">
    <div class="cart">
      <h3>Din beställning</h3>
      <div class="cart-items">
        <CartItem v-for="(item,index) in cart" :key="index" :item="item" />
      </div>
      <div class="totalamount">
        <h3>
          Total
          <!-- <span class="dots"></span> -->
          {{ totalamount }} kr
        </h3>
        <p>Inkl moms + drönarleverans</p>
      </div>
      <a href class="button" @click.prevent="makeOrder">Take My Money</a>
    </div>
  </div>
</template>

<script>
import CartItem from "./CartItem";
export default {
  name: "Cart",
  components: { CartItem },
  computed: {
    cart() {
      return this.$store.state.cart;
    },
    totalamount() {
      return this.$store.state.cart.reduce((acc, item) => acc + item.price * item.quantity, 0);
    }
  },
  methods: {
    makeOrder() {
      this.$store.dispatch("makeOrder");
      this.$router.push("/status");
    }
  }
};
</script>

<style lang="scss" scoped>
.cartview {
  position: absolute;
  top: 100%; /* Place it just below the carticon */
  right: 0;  /* Align to the right edge of the cart-wrapper or icon */
  width: 350px;
  padding: 1rem;
  background: #fff;
  box-shadow: 0 0 1rem rgba(0,0,0,0.2);
  border-radius: 8px;
  z-index: 10;

  .cart {
    display: flex;
    flex-direction: column;
    gap: 1rem;

    h3 {
      font-family: "PT Serif", serif;
      font-weight: bold;
      font-size: 24px;
      margin: 0;
      line-height: 1.2;
    }

    .cart-items {
      display: flex;
      flex-direction: column;
      gap: 1rem;
    }

    .totalamount {
      margin-top: 1rem;
      h3 {
        display: flex;
        align-items: center;
        font-size: 18px;
        margin: 0;
        line-height: 1.2;

        // .dots {
        //   flex: 1;
        //   border-bottom: 2px dotted black;
        //   margin: 0 0.5rem;
        // }
      }
      p {
        margin: 0.5rem 0 0;
        font-size: 14px;
      }
    }

    .button {
      display: inline-flex;
      justify-content: center;
      align-items: center;
      text-decoration: none;
      font-size: 1rem;
      height: 3rem;
      width: 100%;
      border-radius: 50px;
      background: black;
      color: #fff;
      cursor: pointer;
      margin-top: 1rem;

      &:hover {
        background: #222;
      }
      &:active {
        background: #000;
      }
    }
  }
}
</style>
