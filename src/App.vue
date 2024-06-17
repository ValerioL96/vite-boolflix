<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default {
 components:{
  AppHeader,
  AppMain,
 },

  data(){
    return{
      
    }
  }
}

</script>

<template>

<AppHeader />
<AppMain />

</template>

<style lang="scss">
@use '../node_modules/bootstrap/scss/bootstrap.scss';
@use './styles/partials/mixins' as *;
@use './styles/partials/variables' as *;
@use './styles/general';
</style>
