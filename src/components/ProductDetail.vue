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
  return props.products.find((product) => {
    return product.id == productId.value
  })
})
</script>

<template>
  <h2>Producte: {{ product?.name }}</h2>
  <p>Descripcio: {{ product?.description }}</p>
</template>

<style scoped>
h2 {
  margin: 1em 0em 0em;
}
</style>
