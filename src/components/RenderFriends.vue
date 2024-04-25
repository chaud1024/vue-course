<script setup>
import { ref } from 'vue'

const friends = ref(['Johanson', 'Alex', 'Harry', 'Emma', 'Michael'])
</script>

<template>
  <div>
    <h3 v-for="friend in friends" :key="friend">
      {{ friend }}
    </h3>
  </div>
</template>

<style lang="scss" scoped></style>
