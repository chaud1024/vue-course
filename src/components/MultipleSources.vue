<script setup>
import { ref, watch } from 'vue'

const username = ref('Alice')
const counter = ref(0)

watch([username, counter], (newValues, oldValues) => {
  console.log('new values', newValues)
  console.log('old values', oldValues)
})
</script>

<template>
  <div>
    <h1>{{ username }}</h1>
    <h1>{{ counter }}</h1>

    <button @click="username = 'Brown'">Change Name</button>
    <button @click="counter++">Increment</button>
  </div>
</template>

<style lang="scss" scoped></style>
