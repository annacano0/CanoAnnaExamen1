<script setup>
const products = [
  { id: 1, nom: 'Pebrot', descripcio: 'pebrot del penedes de proximitat' },
  { id: 2, nom: 'Tomaquet', descripcio: 'Tomaquet del penedes de proximitat' },
  { id: 3, nom: 'All', descripcio: 'All del penedes de proximitat' },
]
</script>

<template>
  <main>
    <h1>Exercici 1</h1>
    <ul>
      <li v-for="product in products" :key="product.id">
        <router-link :to="{ name: 'product.detail', params: { productId: product.id } }">{{
          product.name
        }}</router-link>
      </li>
    </ul>
    <RouterView></RouterView>
  </main>
</template>
