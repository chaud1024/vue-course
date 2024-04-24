<script setup>
import { reactive } from 'vue'

let object = {
  val: { count: 0 },
  user: ['John', 'Doe']
}

let initialState = reactive(object)

const changeUser = () => {
  ;(initialState.user[0] = 'Michael'), (initialState.user[1] = 'Jackson')
}

const addUser = () => {
  initialState.user.push('Agathe', 'Conney')
}
</script>

<template>
  <div>
    <h1>Reactive</h1>
    <h2>Current Count : {{ initialState.val.count }}</h2>
    <h2>UserL {{ initialState.user }}</h2>

    <button @click="initialState.val.count += 10">Add 10</button>
    <button @click="changeUser">Change User</button>
    <button @click="addUser">Add an User</button>
  </div>
</template>

<style lang="scss" scoped></style>
