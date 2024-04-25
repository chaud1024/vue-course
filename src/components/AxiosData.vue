<script setup>
import { ref } from 'vue'
import axios from 'axios'

const data = ref(null)

const fetchData = async () => {
  try {
    // make a GET request using axios
    const res = await axios.get('https://jsonplaceholder.typicode.com/posts')

    // handle the successful res
    data.value = res.data
  } catch (error) {
    console.error(`Error!: ${error}`)
  }
}
</script>
<template>
  <div>
    <h1>(( Using Axios ))</h1>
    <button @click="fetchData">Fetch Data</button>
  </div>

  <div>
    <h2>Data from Axios</h2>
    <pre>{{ data }}</pre>
  </div>
</template>

<style lang="scss" scoped></style>
