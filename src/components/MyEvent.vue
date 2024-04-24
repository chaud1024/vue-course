<script setup>
import { ref } from 'vue'
let count = ref(0)

const IncrementCount = () => count.value++
const DecrementCount = () => count.value--

const area = ref(null)
const handleSubmit = (e) => {
  e.preventDefault()

  area.value = `Hello ${e.target[0].value} your email is ${e.target[1].value}`
}
</script>
<template>
  <div>
    <h1>Count : {{ count }}</h1>
    <button @click="IncrementCount">Increment</button>
    <button @click="DecrementCount">Decrement</button>
  </div>

  <div>
    <form @:submit="handleSubmit">
      <input type="text" placeholder="Ennter your name" />
      <input type="email" placeholder="Ennter your email" />
      <button type="submit">Submit</button>
    </form>
    <div class="area">{{ area }}</div>
  </div>
</template>

<style lang="scss" scoped></style>
