<script setup>
import LifecycleComponent from './components/LifecycleComponent.vue'

import { ref } from 'vue'
const showHide = ref(true)
</script>

<template>
  <div>
    <LifecycleComponent v-if="showHide" />
    <button @click="showHide = !showHide">Show / Hide</button>
  </div>
</template>

<style scoped></style>
