<script setup>
import { inject } from 'vue'
const emit = defineEmits(['increment'])

const counter = inject('counter')

const increment = () => {
  emit('increment', counter.value + 1)
}
</script>

<template>
  <button @click="increment">+1</button>
</template>
