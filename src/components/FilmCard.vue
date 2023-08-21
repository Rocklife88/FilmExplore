<template>
  <div class="card">
    <img :src="film.poster" alt="Card Image" class="card-image" />
    <div class="card-content">
      <h2 class="card-title">{{ film.title }}</h2>
      <p class="card-paragraph">{{ film.release_year }}</p>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  film: Object
});
</script>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  border: 1px solid #ccc;
  width: 300px;
  height: 350px;
  border-radius: 8px;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
}

.card-image {
  width: 100%;
  height: 150px;
  border-radius: 4px 4px 0 0;
}

.card-content {
  flex: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  padding: 20px;
}

.card-title {
  font-size: 1.5rem;
}

.card-paragraph {
  font-size: 1rem;
}
</style>
