<script>
import SearchBar from './components/SearchBar.vue';

export default {
 components:{
  SearchBar,
 },

  data(){
    return{

    }
  }
}

</script>

<template>

<SearchBar />

</template>

<style lang="scss">
@use '../node_modules/bootstrap/scss/bootstrap.scss';
@use './styles/partials/mixins' as *;
@use './styles/partials/variables' as *;
@use './styles/general';
</style>
