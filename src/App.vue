<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Header from './components/Header.vue';
import Footer from './components/Footer.Vue'

</script>

<template>
  <div class="container">
    <Header/>
    </div>
    <Footer/>

  <RouterView />
</template>

<style scoped>
.container{
  max-width:1100px;
  margin:0 auto;
}



</style>
