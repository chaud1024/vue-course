<script setup>
const props = defineProps(['firstName', 'lastName'])
</script>

<template>
  <div>
    <h1>Hello, {{ props.firstName }} {{ props.lastName }}</h1>
  </div>
</template>

<style lang="scss" scoped></style>
