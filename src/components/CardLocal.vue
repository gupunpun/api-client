<template>
  <div class="card">
    <img :src="anime.img" height="150" width="150" >
    <p class="card-title">{{ anime.name }}</p>
    <ul class="card-description">
      <li>Date realesed: {{ anime.daterealese }}</li>
      <li>Seasons: {{ anime.seasons }}</li>
      <li>Rating: {{ anime.rating }}</li>
      <li>Main character: {{ anime.mc }}</li>
      <li>Villain: {{ anime.villain }}</li>
    </ul>
  </div>
  
</template>

<script>
export default {


    name:'CardLocal',
    props: {
        anime: {
            type: Object,
            required: true
        }
    },
   

}
</script>

<style>

</style>