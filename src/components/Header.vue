<script setup>
import { RouterLink } from 'vue-router';


</script>

<template>
    <div class="header">
<div class="logo-wrapper">
  <RouterLink class="logo" to="/"><h2 class="logo">FilmExplorer</h2></RouterLink>

</div>

    <div class="link-wrapper">
    <RouterLink class="nav-link" to="/">Home</RouterLink>
    <RouterLink class="nav-link" to="/about">About</RouterLink>
</div>
</div>

</template>


<style scoped>


.header{
    display:flex;
    gap:1rem;
    padding:0.3rem 1rem;
    height:5rem;
    align-items: center;
    justify-content: space-between;
    margin-bottom:rem;
  
  }

  .logo{
    color:aquamarine;
    font-weight: 600;
    text-decoration: none;
    cursor: pointer;
  }

  .link-wrapper{
    display:flex;
    align-items:center;
    gap:1rem;
  }
  
  .nav-link{
    text-decoration:none;
    color:white;
    font-size:1.1rem;
    font-weight:500;
    cursor:pointer;
    transition: all 0.4s;
  
  }
  
  .nav-link:hover{
    color:aquamarine
  }

  @media (max-width: 768px) { 
  .header{
    flex-direction:column;
    justify-content: center;
    align-items: center;
    margin-top:1rem;
  }
}
  
</style>