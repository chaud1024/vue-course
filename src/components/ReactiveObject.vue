<script setup>
import { reactive, watch } from 'vue'

const state = reactive({ username: 'Alice' })

watch(
  () => state.username,
  (newValue, oldValue) => {
    console.log('new value', newValue)
    console.log('old value', oldValue)
  }
)
</script>

<template>
  <div>
    <h1>{{ state.username }}</h1>
    <button @click="state.username = 'Bobby'">Change Name</button>
  </div>
</template>

<style lang="scss" scoped></style>
