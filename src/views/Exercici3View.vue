<script setup>
import { ref, computed, watch } from 'vue'
const users = [
  { id: 1, name: 'Anna' },
  { id: 2, name: 'Maria' },
  { id: 3, name: 'Julia' },
  { id: 4, name: 'Thalia' },
  { id: 5, name: 'Juana' },
]
const filter = ref('')

const filteredUsers = computed(() => {
  if (filter.value == '') return users
  return users.filter((user) => user.name.toLocaleLowerCase() === filter.value.toLocaleLowerCase())
})

watch(filter, (newFilter) => {
  console.log('Filtre canviat', newFilter)
})
</script>

<template>
  <main>
    <h1>Exercici 3</h1>
    <input v-model="filter" placeholder="Cerca per nom" />
    <ul v-for="user in filteredUsers" :key="user.id">
      <li>{{ user.name }}</li>
    </ul>
  </main>
</template>
