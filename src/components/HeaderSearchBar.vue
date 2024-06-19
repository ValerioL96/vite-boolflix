<script>
import { store } from '../store.js';

import axios from 'axios';

export default {
 components:{
 },

  data(){
    return{
      store,
    }
  },
  methods: {
        search() {
            if (store.search != '') {
  
                axios.get('https://api.themoviedb.org/3/search/movie', {
                    params: {
                        api_key: 'fb70970567a3c9007af5c8ada3133a9c',
                    }
                })
                .then(response => {
                  console.log(response.data.results);
                  
                  store.movies = response.data.results;
                  store.movies.forEach(content => {
                        try {
                            content.langImg = require('../../assets/img/flags/' + content.original_language + '.png');
                        }
                        catch(err) {
                            content.langImg = null;
                        }
                        content.vote = Math.floor(content.vote_average / 2);
                    });
                });
                axios.get('https://api.themoviedb.org/3/search/tv', {
                    params: {
                        api_key: 'fb70970567a3c9007af5c8ada3133a9c',
                        query: store.search,
                        language: 'it-IT'
                    }
                })
                .then(response => {
                    store.series = response.data.results;
                    store.series.forEach(content => {
                        try {
                            content.langImg = require('../../assets/img/flags/' + content.original_language + '.png');
                        }
                        catch(err) {
                            content.langImg = null;
                        }
                        content.vote = Math.floor(content.vote_average / 2);
                    });
                });
            } else {
                store.movies = [];
                store.series = [];

            }
        }
    }
}

</script>

<template>

<div class="input-group mb-3">
  <input type="text" class="form-control" placeholder="Search for movies" aria-label="Search for movies" aria-describedby="button-addon2" 
   v-model="store.search" @keyup="search()">
  <button class="btn btn-outline-secondary" type="button" id="button-addon2" @click="search()">
  Search
</button>
</div>

</template>

<style scoped lang="scss">

</style>