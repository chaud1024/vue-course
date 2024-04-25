<script setup>
import { ref, watch } from 'vue'

const message = ref('Hello, vue!')
const inputText = ref('')

// Watch for changes in inputText and update message accordingly
watch(inputText, (newValue, oldValue) => {
  // You can perform any logic here when inputText changes
  console.log(newValue, oldValue)
  message.value = `You typed: ${newValue}`
})
</script>
<template>
  <div>
    <h1>{{ message }}</h1>
    <input v-model="inputText" placeholder="Enter something" />
  </div>
</template>

<style lang="scss" scoped></style>
