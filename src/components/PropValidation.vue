<script setup>
// const props = defineProps({
//   fullName: String,
//   age: Number
// })

const props = defineProps({
  fullName: {
    type: String,
    required: true,
    defualt: 'Paul'
  },
  age: Number
})
</script>

<template>
  <div>
    <h1>{{ props.fullName }}</h1>
    <h1>{{ props.age }}</h1>
  </div>
</template>

<style lang="scss" scoped></style>
