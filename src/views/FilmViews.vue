<template>
    <div class="container">
        <div class="card">
      <h1 v-if="film">{{film.title}}</h1>
      <p v-if="film"> Year: {{ film.release_year }}</p>
      <p v-if="film">{{film.description}}</p>
      <img class="image" :src="film.poster" alt="">
    </div>
    </div>
  </template>
  
  <script setup>
  import { useRoute } from 'vue-router';
  import FilmData from '../data/filmList.json';
  
  const route = useRoute();
  const filmId = Number(route.params.id);
  

  

  const film = FilmData.find(film => film.id === filmId);
  
  </script>
  
  <style scoped>

  .container{
max-width:1100px;
margin:0 auto;
text-align: center;


  }
  .card{
    display:flex;
    flex-direction: column;
    padding:3rem;
    width:600px;
    max-height:800px;
    border:0.6px solid aquamarine;
    border-radius:0.5rem;
    margin: 0 auto;
    margin-top:4rem;
  }

  h1, p, img{
    padding: 0.3rem ;
    line-height:1.3;
    text-align: left;
    margin-bottom:1.2rem;
  }

  p{
    font-size:1.2rem;
    color:#f9f9f9;
  }

  h1{
    font-size:3rem;
    color:aquamarine;
  }


  .image{
    width:90%;
height:100%;
border-radius:1rem;

  }


    @media (max-width: 768px) {
      .card {
        max-width: 350px;
        max-height: none; 
        margin: 0 auto;
        margin-top:2.5rem;
      }

      h1{
        font-size:1.8rem;
      }
    
      .image {
        width: 100%; 
        height: auto; 
      }
    }
  </style>
  
  
