<script setup>
import { useCounter } from '../shared/useCounter'

const counter = useCounter()
</script>

<template>
  <div>
    <h1>Counter</h1>
    <h2>{{ counter.count }}</h2>
    <button @click="counter.increment">Increment</button>
    <button @click="counter.decrement">Decrement</button>
  </div>
</template>

<style lang="scss" scoped></style>
