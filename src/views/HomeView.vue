<script setup>
import {ref, computed} from 'vue'
import { RouterLink } from 'vue-router';
import FilmCard from '../components/FilmCard.vue'
import FilmData from '../data/filmList.json'

const films = ref(FilmData)


const filteredFilms = computed(() =>{
return films.value.filter( film => film.title.toLowerCase().includes(search.value.toLowerCase()))

})



const search =ref('');

</script>
<template>
  <div class="container">
    <div class="header">
      <input v-model="search" type="text" placeholder="Search..." class="input-text">
    </div>
    <div class="card-container">
      <RouterLink class="nav-link" :to="`/films/${film.id}`" v-for="film in filteredFilms" :key="film.id">
        <FilmCard :film="film"/>
      </RouterLink>
    </div>
  </div>
</template>

<style scoped>
.container {
  max-width: 1100px;
  margin: 0 auto;
  padding: 1rem;
}

.header {
  margin-bottom: 1.5rem;
}

.input-container {
  display: flex;
  justify-content: center;
}

.input-text {
  padding: 1rem 2rem 1rem;
  font-size: 1rem;
  text-align: left;
}

.input-text::placeholder {
  text-align: left;
}

.card-container {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  gap: 0.8rem;
  padding-bottom: 8rem;
  margin-top:3rem;
  margin: 0 auto;
  align-items: flex-start; 

}

.nav-link {
  text-decoration: none;
  color: white;
  font-size: 1.1rem;
  font-weight: 500;
  cursor: pointer;
  transition: all 0.4s;
}

.nav-link:hover {
  color: aquamarine;
}

@media (max-width: 768px) {
  .card-container {
    justify-content: center; 
  }

  .container {
    text-align: center;
  }
}
</style>
