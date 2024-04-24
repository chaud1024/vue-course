<script setup>
defineProps({
  friends: Array,
  userInfo: Object
})
</script>

<template>
  <div>
    <h1>{{ friends }}</h1>
    <h1>{{ userInfo }}</h1>

    <hr />

    <ul v-for="(friend, index) in friends" :key="index">
      <li>{{ friend }}</li>
    </ul>

    <ul v-for="(info, index) in userInfo" :key="index">
      <li>{{ info }}</li>
    </ul>
  </div>
</template>

<style lang="scss" scoped></style>
