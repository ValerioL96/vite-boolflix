<script>
import { store } from '../store.js';
import Card from './Card.vue';


export default {
    
    components: {
        Card,
    },

    props: {
        content:{
            type: Array,
            required: true,
        }
    },
    
    data() {
        return {
            store,
        }
    }
}
</script>

<template>
    <section>
        <h2>Movies</h2>
        <div class="cards">
            <Card v-for="(content, index) in store.movies" :key="index" :content="content"/>
        </div>
    </section>
</template>

<style lang="scss" scoped>

.cards {
    display: grid;
    grid-template-columns: repeat(auto-fill, 250px);
    grid-gap: 30px;
}
</style>