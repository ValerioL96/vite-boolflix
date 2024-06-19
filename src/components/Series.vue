<script>
import { store } from '../store.js';
import Card from './Card.vue';

export default {

    components: {
        Card,
    },
    data() {
        return {
            data
        }
    }
}
</script>

<template>
    <section>
        <h2>Series</h2>
        <div class="cards">
            <Card v-for="(content, index) in store.series" :key="index" :content="content"/>
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