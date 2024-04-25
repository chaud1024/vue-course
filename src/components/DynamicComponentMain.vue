<script setup>
import { ref } from 'vue'

import DynamicComponentOne from './DynamicComponentOne.vue'
import DynamicComponentTwo from './DynamicComponentTwo.vue'
import DynamicComponentThree from './DynamicComponentThree.vue'

const currentTab = ref('DynamicComponentOne')

const tabs = {
  DynamicComponentOne,
  DynamicComponentTwo,
  DynamicComponentThree
}
</script>

<template>
  <div>
    <h1>Dynamic Component Main</h1>
    <button @click="currentTab = 'DynamicComponentOne'">What is HTML?</button>
    <button @click="currentTab = 'DynamicComponentTwo'">What is CSS?</button>
    <button @click="currentTab = 'DynamicComponentThree'">What is JS?</button>
  </div>
  <div>
    <component :is="tabs[currentTab]"></component>
  </div>
</template>

<style lang="scss" scoped></style>
