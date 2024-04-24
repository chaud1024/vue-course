<script setup>
import { ref, computed } from 'vue'

const initialNum = ref(5)

const sqaruedNum = computed(() => {
  return initialNum.value * initialNum.value
})

const counter = ref(0)
const squaredCounter = computed(() => {
  return counter.value ** 2
})
const incrementCounter = () => {
  counter.value++
}
</script>
<template>
  <div>
    <h1>Initial Number : {{ initialNum }}</h1>
    <h1>Squared Number : {{ sqaruedNum }}</h1>
    <hr />

    <h1>Counter : {{ counter }}</h1>
    <p>Squared Counter : {{ squaredCounter }}</p>
    <button @click="incrementCounter">Increment</button>
  </div>
</template>

<style lang="scss" scoped></style>
