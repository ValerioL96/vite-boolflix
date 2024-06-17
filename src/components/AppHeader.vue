<script>
import HeaderSearchBar from './HeaderSearchBar.vue';
import { store } from '../store.js';

export default {
 components:{
  HeaderSearchBar,
 },

  data(){
    return{
      store,
    }
  },

  methods:{
    searchMovies(searchedString){
      console.log('Clicked');
      this.store.searchedString;
    }
  }
   
}

</script>

<template>

<HeaderSearchBar @searched="searchMovies" />

</template>

<style scoped>

</style>