<template>
  <h2>Cart Options API</h2>
</template>

<script>
export default {
  data() {
    return {
      cart: [],
      products: []
    }
  },
  computed: {
    showCartInfo() {
      return "O carrinho de compras tem" + this.cart.length + "produtos";
    },

    showProductsInfo() {
      return "A lista de produtos tem" + this.products.length + "produtos";
    }
  },
  
  methods: {
    cartRemove(index) {
      this.cart.splice(index, 1);
    },

    productRemove(index) {
      this.products.splice(index, 1)
    }
  }
}

</script>