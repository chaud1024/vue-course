<script setup>
import { ref } from 'vue'

let arrayPeople = [
  {
    name: 'John',
    major: 'Math'
  },
  {
    name: 'Jullieth',
    major: 'Physics'
  },
  {
    name: 'James',
    major: 'Chemistry'
  },
  {
    name: 'Johanson',
    major: 'Biology'
  }
]
let people = ref(arrayPeople)

let movieArray = [
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
    genre: ['Drama', 'Mystery', 'Sci-Fi'],
    year: 2006,
    casts: ['Christian Bale', 'Hugh Jackman', 'Scarlett Johansson']
  }
]
let movies = ref(movieArray)

const formData = ref({ username: '', email: '', password: '' })
</script>

<template>
  <h1>V-for</h1>
  <div>
    <h2>Students</h2>
    <ul>
      <li v-for="({ name, major }, index) in people" :key="index">
        <span>{{ name }} | </span>
        <span>{{ major }}</span>
      </li>
    </ul>
  </div>
  <hr />
  <div>
    <h2>Movies</h2>
    <ul>
      <li v-for="({ title, genre, year, casts }, index) in movies" :key="index">
        <p>
          <strong>{{ title }}</strong> | <span>{{ genre.join(', ') }}</span>
        </p>
        <p>Release Date: {{ year }}</p>
        <p>Casting : {{ casts.join(', ') }}</p>
      </li>
    </ul>
  </div>
  <hr />
  <div>
    <form @submit.prevent>
      <input type="text" placeholder="Enter your name" v-model="formData.username" />
      <input type="email" placeholder="Enter your email" v-model="formData.email" />
      <input type="password" placeholder="Enter your password" v-model="formData.password" />
      <button type="submit">Submit</button>
    </form>

    <h1>{{ formData.username }}</h1>
    <h1>{{ formData.email }}</h1>
    <h1>{{ formData.password }}</h1>
  </div>
</template>

<style lang="scss" scoped>
form {
  width: 200px;
  display: flex;
  flex-direction: column;
  gap: 5px;
}
</style>
