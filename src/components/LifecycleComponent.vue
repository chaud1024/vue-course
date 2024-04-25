<script setup>
import {
  ref,
  onBeforeMount,
  onMounted,
  onBeforeUpdate,
  onUpdated,
  onBeforeUnmount,
  onUnmounted
} from 'vue'

const message = ref('Hello, vue!')

// Lifecycle hooks
onBeforeMount(() => {
  console.log('Component is about to be mounted')
})

onMounted(() => {
  console.log('Component has been mounted')
})

const updateMessage = () => {
  message.value = 'Updated message'
}

onBeforeUpdate(() => {
  console.log('Component is about to be updated')
})

onUpdated(() => {
  console.log('Component has been updated')
})

onBeforeUnmount(() => {
  console.log('Component is about to be unmounted')
})

onUnmounted(() => {
  console.log('Component has been unmounted')
})
</script>

<template>
  <div>
    <p>{{ message }}</p>
    <button @click="updateMessage">Update message</button>
  </div>
</template>

<style lang="scss" scoped></style>
