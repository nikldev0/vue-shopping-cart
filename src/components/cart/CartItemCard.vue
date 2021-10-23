<template>
  <div class="cart-item-card">
    <div class="header">
      <h4>{{ product.name }}</h4>
      <h4>In Cart: {{ product.quantity }}</h4>
      <h4>Total Cost: £ {{ item_cost.toFixed(2) }}</h4>
    </div>
    <p>{{ description }}</p>
  </div>
</template>

<script>
export default {
  name: "CartItemCard",
  props: {
    product: {
      type: Object,
      required: true,
    },
  },
  computed: {
    description() {
      return this.product.description.substring(0, 120);
    },

    item_cost() {
      return this.product.price * this.product.quantity;
    },
  },
};
</script>

<style lang="scss" scoped>
.cart-item-card {
  width: 90%;
  margin: 5%;
  background-color: 0 0 5px grey;
  border-radius: 5%;
  padding: 10px;
  text-align: left;

  .header {
    display: flex;
    justify-content: space-around;
  }
}
</style>
