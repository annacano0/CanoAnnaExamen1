<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <div class="wrapper">
      <nav>
        <router-link to="/">Home</router-link>
        <router-link to="/exercici1">Exercici 1</router-link>
        <router-link to="/exercici2">Exerici 2</router-link>
        <router-link to="/exercici3">Exerici 3</router-link>
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style scoped></style>
