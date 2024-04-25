<script setup>
import { ref } from 'vue'

const data = ref(null)

const fetchData = async () => {
  // make a get request using fetch
  await fetch('https://jsonplaceholder.typicode.com/posts')
    .then((res) => {
      if (!res.ok) {
        throw new Error('http error')
      }
      return res.json()
    })
    .then((resData) => {
      data.value = resData
    })
    .catch((error) => console.error(error))
}
</script>

<template>
  <div>
    <h1>(( Using Fetch))</h1>
    <button @click="fetchData">fetchData</button>
    <div>
      <h2>Data from Fetch</h2>
      <pre>{{ data }}</pre>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
