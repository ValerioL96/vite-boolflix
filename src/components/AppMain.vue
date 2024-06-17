<script>
import axios from 'axios';

export default {
 components:{
 },

  data(){
    return{
      movies:[],
    }
  },
  methods:{
    getMovies(movieTitle){
        axios.get('https://api.themoviedb.org/3/search/movie?api_key=fb70970567a3c9007af5c8ada3133a9c&query=road' + movieTitle)
  .then((response) =>{
    
    console.log(response.data.results);
    this.movies=response.data.results;
  })
  .catch(function (error) {
    
    console.log(error);
  })
  .finally(function () {
    
  });
    }
  },
  created(){
    this.getMovies();
  }
}

</script>

<template>

<ul >
    <li v-for="movie in movies" :key="movie.id" >

        <h3>
            titolo: {{ movie.title }}
        </h3>
        <h3>
            titolo originale: {{ movie.original_title }}
        </h3>
        <h3>
            voto: {{ movie.vote_average }}
        </h3>
        <h3>
            lingua: {{ movie.original_language }}
        </h3>
        
    </li>
   
</ul>

</template>

<style scoped lang="scss">

</style>