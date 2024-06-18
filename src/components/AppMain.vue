<script>
import MainCards from './MainCards.vue'


export default {

  components: {
      MainCards,
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
      <MainCards />
  </main>
</template>

<style lang="scss" scoped>


</style>