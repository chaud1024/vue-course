<script setup>
const props = defineProps(['name'])
</script>
<template>
  <div>
    <h1>Hello, {{ props.name }}</h1>
  </div>
</template>

<style lang="scss" scoped></style>
