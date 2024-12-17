<script setup>
import { inject } from 'vue'
const emit = defineEmits(['decrement'])

const counter = inject('counter')

const decrement = () => {
  emit('decrement', counter.value - 1)
}
</script>

<template>
  <button @click="decrement">-1</button>
</template>
