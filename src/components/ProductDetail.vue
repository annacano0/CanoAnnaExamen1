<script setup>
import { defineProps } from 'vue'
import { computed } from 'vue'
import { useRoute } from 'vue-router'

const route = useRoute()

const props = defineProps({
  products: {
    type: Array,
    required: true,
  },
})

const productId = computed(() => {
  return route.params.productId
})

const product = computed(() => {
  console.log(props.products, productId.value)
  return props.products?.find((product) => {
    product.id === parseInt(productId.value)
  })
})
</script>

<template>
  <h2>Producte: {{ product?.name }}</h2>
  <p>id: {{ productId }}</p>
  <p>Descripcio: {{ product?.description }}</p>
</template>
