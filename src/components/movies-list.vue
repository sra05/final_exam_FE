<template>
    <div class="sub-container">
        <h1>Movies List</h1>
        <div class="movies-list">
            <section class="movie-section" v-for="movie in movies" :key="movie.movie_title" >
            <movieCard :movie="movie" />
        </section>
        </div>
    </div>
</template>
<script>
import movieCard from './movie-card.vue'
export default {
   props: {
    movies: Array
   },
   components: {movieCard}
}
</script>
<style>
.movie-section{
    box-shadow: #fbfafaf2 0px 5px 15px;
    
}
.sub-container{
    width: 50%;
    margin: auto;
    padding: 15px;
    font-family: 'Playfair Display', serif;
    
}
.sub-container h1 {
    text-align: center;
   
}
</style>