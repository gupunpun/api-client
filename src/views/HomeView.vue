<template>
 <div>
  <h4 class="type">Cartões</h4>

  <div class="container">
    <div v-for="film in films" :key="film.id">
      <card :film="film"></card>
    
    </div>
  </div>
</div>
</template>

<script>
  import Card from '../components/Card.vue'

    const API_URL = 'https://ghibliapi.vercel.app/films'

    export default {
        data() {
            return {
                films: []
            };
        },
        methods: {
            async getGhibli() {
                const response = await fetch(API_URL);
                const data = await response.json();
                this.films = data;
            }
        },
        created() {
            this.getGhibli();
        },
        components: {
            Card
        }
    }
    
  </script>

  <style>
  body {
    background-color: rgb(235, 203, 203);
  }
  
  .title {
    color: #ff8d8d;
  }
  
  .type {
    color: rgb(0, 0, 0);
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    text-align: center;
  }
  
  .row {
    text-align: start;
    align-content: center;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
    margin: 0;
  }
  
  .header {
    color: #FFE807;
    font-weight: bold;
    font-size: 14px;
    background-color: #121212 !important;
  }
  
  .row li {
    background-color: white;
    display: inline-block;
    padding: 10px;
    border: 1px solid black;
  }
  
  .col-l {
    width: 100px;
  }
  
  .col-m {
    width: 200px;
  }
  
  .col-g {
    width: 250px;
  }
  
  .container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    width: 100%;
  }
  
  .card {
    background-color: rgb(229, 209, 209);
    border-radius: 10px;
    margin: 20px;
    height: 350px;
    width: 250px;
    text-align: center;
    align-content: center;
    font-family: Verdana, Geneva, Tahoma, sans-serif;
  }
  
  .card-title {
    color: #1f1f1c;
    font-size: 20px;
    font-weight: bold;
    text-shadow: 1px 1px 5px black;
  }
  
  .card-description {
    font-size: 14px;
    text-align: start;
    padding-left: 50px;
  }
  </style>
