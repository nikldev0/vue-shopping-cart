<template>
  <div class="cart-item-card">
    <h3>Cart Total: £ {{ cart_total.toFixed(2) }}</h3>

    <button class="view-product-button">Pay by Credit Card</button>
  </div>
</template>

<script>
export default {
  name: "CartSummaryPaymentCard",
  computed: {
    cart_total() {
      return this.$store.getters.cartTotal;
    },
  },
};
</script>

<style lang="scss" scoped>
.view-product-button {
  padding: 0.5rem 7rem;
  border-radius: 0.2rem;
  background-color: rgb(36, 62, 54);
  color: #e0eec6;
  border: none;
  font-size: 1rem;
  cursor: pointer;

  &:hover {
    background-color: rgba(36, 62, 54, 0.9);
  }
}
</style>
