<template>
  <h2>Cart Composition API</h2>
</template>

<script setup>
import { reactive, computed } from 'vue';

// cart
const cart = reactive(data:[]);
function cartRemove(index) {
  cart['data'].splice(index, 1);
}
const showCartInfo = computed(() => {
  return "O carrinho de compras tem " + cart['data'].length + " produtos"
})

// product
const products = reactive(data:[]);
function productRemove(index) {
  products['data'].splice(index, 1)
}
const showProductsInfo = computed(() => {
  return "A lista de produtos tem " + cart['data'].length + " produtos";
})

</script>