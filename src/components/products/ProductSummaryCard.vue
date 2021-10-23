<template>
  <div class="productCard">
    <h3>{{ product.name }}</h3>
    <h5>Price: £ {{ product.price.toFixed(2) }}</h5>
    <p class="description">{{ description }}</p>
    <p class="text-muted">
      <em>{{ product.category }}</em>
    </p>
    <button class="view-product-button" @click="$emit('view-product', product)">
      View Product
    </button>
  </div>
</template>

<script>
// import items from "../data/items.js";

export default {
  name: "ProductSummaryCard",
  props: {
    product: {
      type: Object,
      required: true,
    },
  },
  computed: {
    description() {
      return this.product.description.substring(0, 150);
    },
  },
};
</script>

<style lang="scss" scoped>
.productCard {
  padding: 1rem;
  margin: 1rem;
  box-shadow: 0 1px 2px rgba(0, 0, 0, 0.07), 0 2px 4px rgba(0, 0, 0, 0.07),
    0 4px 8px rgba(0, 0, 0, 0.07), 0 8px 16px rgba(0, 0, 0, 0.07),
    0 16px 32px rgba(0, 0, 0, 0.07), 0 32px 64px rgba(0, 0, 0, 0.07);
  transition: 0.5s all ease-in-out;

  &:hover {
    transform: translateY(-10px);
    transition: 0.5s all ease-in-out;
  }

  h3 {
    font-size: 1.6rem;
  }

  .text-muted {
    color: rgb(54, 52, 52);
  }

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
}
</style>
