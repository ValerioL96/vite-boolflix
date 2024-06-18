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
                        query: data.search,
                        language: 'it-IT'
                    }
                })
                .then(response => {
                    store.contents = response.data.results;
                });
            } else {
                store.contents = [];
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