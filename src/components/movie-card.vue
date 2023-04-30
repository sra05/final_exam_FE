<template>
    <div>
        <section class="movie-card">
            <img :src="movie.movie_poster" class="movie-poster" alt="">
            <div class="info">
                <p>Movie Title : {{ movie.movie_title }}</p>
                <p>Relase Date : {{ movie.release_data }}</p>
                <p>Music Director : {{ movie.music_director }}</p>
                <p>Producer : {{ movie.producer }}</p>
                <p>Genre : {{ movie.Genre }}</p>
            </div>
        </section>
    </div>
</template>
<script>
export default {
   props: {
    movie: Object
   }
}
</script>
<style>
.movie-card{
    display: flex;
    gap: 20px;
    padding: 20px;
    background-color: #BFA181;
}
.movie-poster{
    width: 150px;
    height: 150px;
}
.info p{
    font-weight: bold;
    line-height: 30px;
    font-family: 'Roboto Condensed', sans-serif;
    color: white;
    background-color: #BFA181;
}
</style>