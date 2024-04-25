<script setup>
import { inject } from 'vue'

const name = inject('name')
const age = inject('age')
const location = inject('location')
</script>

<template>
  <div>
    <h1>Student</h1>
    <p>{{ name }}</p>
    <p>{{ age }}</p>
    <p>{{ location }}</p>
  </div>
</template>

<style lang="scss" scoped></style>
