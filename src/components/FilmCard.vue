<template>
    <div class="card">
      <img :src="film.poster" alt="Card Image" class="card-image" />
      <h2 class="card-title">{{ film.title }}</h2>
      <p class="card-paragraph">{{ film.release_year }}</p>
    </div>
  </template>
  
  <script setup>
const props = defineProps({
  film: Object
});
  </script>

  
  
  
  <style scoped>
  .card {
    border: 1px solid #ccc;
    width:350px;
    height:350px;
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  .card-image {
  
     width: 100%;
    height:150px;
    border-radius: 4px;
  }
  
  .card-title {
    font-size: 1.5rem;
    margin-top: 10px;
  }
  
  .card-paragraph {
    margin-top: 0.8rem;
  }


  </style>
  