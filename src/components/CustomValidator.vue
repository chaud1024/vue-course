<script setup>
defineProps({
  name: {
    type: String,
    validator: (propValue) => {
      return ['Harry', 'Paul', 'John'].includes(propValue)
    }
  },
  age: {
    type: Number,
    validator: (propValue) => (propValue > 19 && propValue < 40 ? true : false)
  },
  password: {
    type: String,
    validator: (propValue) => propValue.length >= 8
  }
})
</script>

<template>
  <div>Name: {{ name }}</div>
  <div>Age: {{ age }}</div>
  <div>PW: {{ password }}</div>
</template>

<style lang="scss" scoped></style>
