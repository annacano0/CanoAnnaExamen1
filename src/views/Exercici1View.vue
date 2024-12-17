<script setup>
import ProductDetail from '@/components/ProductDetail.vue'

const products = [
  { id: 1, name: 'Pebrot', description: 'pebrot del penedes de proximitat' },
  { id: 2, name: 'Tomaquet', description: 'Tomaquet del penedes de proximitat' },
  { id: 3, name: 'All', description: 'All del penedes de proximitat' },
]
</script>

<template>
  <main>
    <h1>Exercici 1</h1>
    <ul>
      <li v-for="product in products" :key="product.id">
        <router-link
          :products="products"
          :to="{ name: 'product.detail', params: { productId: product.id } }"
          >{{ product.name }}
        </router-link>
      </li>
    </ul>
    <RouterView> <ProductDetail :products="products" /> </RouterView>
  </main>
</template>
