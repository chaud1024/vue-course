<script setup>
import { ref } from 'vue'

import DynamicProps from './components/DynamicProps.vue'
import StaticProps from './components/StaticProps.vue'

import ChangingPropsValues from './components/ChangingPropsValues.vue'
import PropValidation from './components/PropValidation.vue'
import ComplexProps from './components/ComplexProps.vue'

import CustomValidator from './components/CustomValidator.vue'

const firstName = ref('John')
const lastName = ref('Wick')

const favNumber = ref(7)
</script>

<template>
  <StaticProps name="John" />
  <hr />
  <DynamicProps :firstName="firstName" :lastName="lastName" />
  <hr />
  <ChangingPropsValues :favNumber="favNumber" />
  <hr />
  <PropValidation fullName="John Doe" :age="40" />
  <hr />
  <ComplexProps
    :friends="['Johanson', 'Alex', 'Harry']"
    :userInfo="{ name: 'paul', age: 20, location: ['Korea', 'Asia'] }"
  />
  <hr />
  <CustomValidator name="Conney" :age="22" password="impossiblePassword" />
</template>

<style scoped></style>
