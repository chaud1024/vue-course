<script setup>
import FormComponent from './components/FormComponent.vue'

const handleForm = (username, email, password) => {
  console.log(username, email, password)
}
</script>

<template>
  <FormComponent @userInfo="handleForm" />
</template>

<style scoped></style>
