<script setup>
import { onMounted, ref } from 'vue'
import RefComponent2 from './RefComponent2.vue'

const myRef = ref(null)

onMounted(() => {
  console.log(myRef.value)
})
</script>

<template>
  <div>
    <RefComponent2 ref="myRef" />
  </div>
</template>

<style lang="scss" scoped></style>
