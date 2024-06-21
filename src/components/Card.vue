<template>
  <div class="card">
    <img :src="film.movie_banner" height="150" width="150" >
    <p class="card-title">{{ film.original_title_romanised }}</p>
    <ul class="card-description">
      <li>Titulo traduzido: {{ film.title }}</li>
      <li>Diretor: {{ film.director }}</li>
      <li>Lançamento: {{ film.release_date }}</li>
      <li>Score Rotten tomato: {{ film.rt_score }}</li>
    </ul>
  </div>
  
</template>

<script>
export default {


    name:'Card',
    props: {
        film: {
            type: Object,
            required: true
        }
    },
   

}
</script>

<style>

</style>