<script setup>
import { ref, provide } from 'vue'
import BotoRestar from '@/components/BotoRestar.vue'
import BotoSumar from '@/components/BotoSumar.vue'

const counter = ref(0)

provide('counter', counter)

const increment = (newValue) => {
  counter.value = newValue
}
const decrement = (newValue) => {
  counter.value = newValue
}
</script>

<template>
  <main>
    <h1>Comptador</h1>
    <p>Valor comptador: {{ counter }}</p>
    <BotoSumar @increment="increment"></BotoSumar>
    <BotoRestar @decrement="decrement"></BotoRestar>
  </main>
</template>
