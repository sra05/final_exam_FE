<script>
import moviesListVue from './components/movies-list.vue';
export default {
  data() {
    return {
      movies: []
    }
  },
  components: {moviesListVue},
  methods: {
    async getMovies() {
      const res = await fetch('http://localhost:3838/api');
      return await res.json();
    }
  },
  mounted() {
    this.getMovies().then(response => {
      if (response) {
        this.movies = response.data;
      }

    })
  }
}
</script>

<template>
  <div class="main-container">
    <header>
      <h1>TRENDING MOVIES OF SSR</h1>
    </header>
    <moviesListVue :movies="movies" />
  </div>
</template>

<style>
header{
  text-align: center;
  box-shadow: #fbfafaf2 0px 5px 15px;
  padding: 20px 0px;
  font-family: 'Playfair Display', serif;
  color: aliceblue;
}
.main-container{
  background-color: #001233;
  color: aliceblue;
}
</style>
