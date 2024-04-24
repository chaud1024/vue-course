<script setup>
import { ref } from 'vue'

let isVisible = ref(true)

let isUserSignin = ref(true)
let userName = 'John Doe'
let showDetails = ref(isUserSignin)

let password = ref('strongPassword!')
</script>

<template>
  <div>
    <p v-show="isVisible">
      This paragraph will be shown or hidden based on the value of isVisible.(Working with v-show!)
    </p>
    <button @click="isVisible = !isVisible">Toggle</button>
  </div>
  <hr />
  <div>
    <h1 v-if="isUserSignin">Welcome, {{ userName }}!</h1>
    <h1 v-else>Please sign in to access this content.</h1>

    <div v-show="showDetails">
      <h4>You're now able to modify your dashboard.</h4>
    </div>
  </div>
  <hr />
  <div>
    <h1 v-if="password.length > 8">Strong password</h1>
    <h1 v-else-if="password.length < 8">Weak password</h1>
    <h1 v-else>Please Enter Your Password</h1>
  </div>
</template>

<style lang="scss" scoped></style>
