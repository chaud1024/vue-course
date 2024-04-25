<script setup>
import { onMounted, ref } from 'vue'

const myRef = ref('')
console.log(myRef.value)

onMounted(() => {
  console.log(myRef.value)
  myRef.value.focus()
})
</script>

<template>
  <div>
    <input type="text" ref="myRef" placeholder="Enter your name" />
  </div>
</template>

<style lang="scss" scoped></style>
