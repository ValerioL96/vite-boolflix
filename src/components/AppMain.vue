<script>
import Movies from './Movies.vue';
import Series from './Series.vue';


export default {

  components: {
    Movies,
    Series,
  },
  props: {
        content:{
            type: Array,
            required: true,
        }
  },

  data(){
    return{
    
    }
  },
}
</script>

<template>
  <main>

    <Movies />
    <Series />
    
  </main>
</template>

<style lang="scss" scoped>


</style>