<script setup>
import { provide } from 'vue'

import ProvideComponent from './components/ProvideComponent.vue'

provide('name', 'Paul')
provide('age', 20)
provide('location', ['Paris', 'France'])

provide('friends', ['Johanson', 'Alex', 'Harry'])

provide('games', {
  id: 1,
  title: 'Game of Thrones',
  genre: ['Action', 'Fantasy', 'Drama'],
  platform: ['PS4', 'Xbox', 'PC'],
  relaseDate: '2023-03-15',
  developer: {
    name: 'George Martin',
    location: 'San Francisco, USA'
  }
})

provide('movies', [
  {
    title: 'Inception',
    genre: ['Action', 'Sci-Fi', 'Drama'],
    year: 2010,
    casts: ['Leonardo Di Caprio', 'Cillian Murphy', 'Domhnall Gleeson']
  },
  {
    title: 'Interstellar',
    genre: ['Sci-Fi', 'Drama', 'Adventure'],
    year: 2014,
    casts: ['Matthew McConaughey', 'Anne Hathaway', 'Jessica Chastain']
  },
  {
    title: 'The Prestige',
    genre: ['Drama', 'Mystery', 'Thriller'],
    year: 2006,
    casts: ['Christian Bale', 'Hugh Jackman', 'Scarlett Johansson']
  }
])
</script>

<template>
  <div>
    <ProvideComponent />
  </div>
</template>

<style scoped></style>
