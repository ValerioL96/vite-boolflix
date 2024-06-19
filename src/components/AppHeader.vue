<script>
import HeaderSearchBar from './HeaderSearchBar.vue';

export default {
 components:{
  HeaderSearchBar,
 },

  data(){
    return{
    
    }
  },

   
}

</script>

<template>
<header>
  <div class="logo">
    <img src="../assets/img/logo.png" alt="Boolflix logo">
  </div>
  <HeaderSearchBar />
</header>


</template>

<style lang="scss" scoped>

header {
    background-color: rgb(13,13,13);
    height: 70px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 15px 40px;
    .logo, .logo img {
        height: 100%;
    }
}

</style>