<script setup>
import { RouterLink, RouterView } from 'vue-router'
import Header from './components/Header.vue';

</script>

<template>
  <div class="container">
    <Header/>
    </div>
  <RouterView />
</template>

<style scoped>
.container{
  max-width:1100px;
  margin:0 auto;
}



</style>
