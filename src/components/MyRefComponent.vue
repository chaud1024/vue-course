<script setup>
import { reactive, ref } from 'vue'

let count = ref(0)
let userName = ref('')
let userList = ref(['John', 'Doe', 'Michael', 'Jackson'])

let alex = {
  code: 701102,
  name: 'Alex',
  age: 20,
  location: ['NYC', 'IDK'],
  isMarried: false
}
let userInfo = ref(alex)

let friends = reactive([ref('Johanson'), ref('Alex'), ref('Harry')])
</script>
<template>
  <div>
    <h1>Count: {{ count }}</h1>
    <button @click="count++">+</button>
    <button @click="count--">-</button>
    <hr />

    <h1>User: {{ userName }}</h1>
    <button @click="userName = 'Michael'">Add User</button>
    <hr />

    <h1>User List : {{ userList }}</h1>
    <button @click="userList.push('Alice')">Add New User</button>
    <hr />

    <h1>{{ userInfo.name }} Info</h1>
    <ul>
      <li v-for="user in userInfo" :key="user.code">{{ user }}</li>
    </ul>
    <button @click="userInfo.name = 'Harry'">Change Name</button>
    <hr />

    <ol>
      <li>{{ friends[0] }}</li>
      <li>{{ friends[1] }}</li>
      <li>{{ friends[2] }}</li>
    </ol>

    <button @click="friends[0] = '🤝'">Hand Shake</button>
    <button @click="friends[1] = '🤝'">Hand Shake</button>
    <button @click="friends[2] = '🤝'">Hand Shake</button>
  </div>
</template>

<style lang="scss" scoped></style>
