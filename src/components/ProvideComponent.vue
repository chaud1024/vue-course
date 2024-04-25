<script setup>
import { inject } from 'vue'

const friendsList = inject('friends')
const games = inject('games')
const movies = inject('movies')
</script>
<template>
  <h1>Injecting Data</h1>
  <div>
    <ul v-for="(friend, index) in friendsList" :key="index">
      <li>{{ friend }}</li>
    </ul>
  </div>
  <hr />
  <div>
    <ul v-for="(game, index) in games" :key="index">
      <li>
        {{ game }}
      </li>
    </ul>
  </div>
  <hr />
  <div>
    <ul v-for="(movie, index) in movies" :key="index">
      <li>
        {{ movie }}
      </li>
    </ul>
  </div>
  <hr />
  <div>
    <ul v-for="({ title, genre, year, casts }, index) in movies" :key="index">
      <li>{{ title }} | {{ genre.join(', ') }} | {{ year }} | {{ casts.join(', ') }}</li>
    </ul>
  </div>
</template>

<style lang="scss" scoped></style>
