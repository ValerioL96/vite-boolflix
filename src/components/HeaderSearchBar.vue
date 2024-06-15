<script>

import { store } from '../store.js';

export default{
  
  data(){
    return{
      store,
    }
  }
}

</script>

<template>

<div class="input-group mb-3">
  <input type="text" class="form-control" placeholder="Search for movies" aria-label="Search for movies" aria-describedby="button-addon2">
  <button class="btn btn-outline-secondary" type="button" id="button-addon2">Search</button>
</div>

</template>

<style scoped lang="scss">

</style>