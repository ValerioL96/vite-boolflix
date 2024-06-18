<script>
export default {

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
    },
    methods:{
        
    }
}
</script>

<template>
    <div class="card"  >
        <div class="title">
            <span><strong>Titolo: </strong></span>
            <h3 v-if="content.title != undefined">{{content.title}}</h3>
            <h3 v-else>{{content.name}}</h3>
        </div>
        <div class="title-orig">
            <span><strong>Titolo originale: </strong></span>
            <p v-if="content.original_title != undefined">{{content.original_title}}</p>
            <p v-else>{{content.original_name}}</p>
        </div>
        <div class="lang">
            <span><strong>Lingua: </strong></span>
            <img v-if="content.langImg != null" :src="content.langImg" :alt="content.title + ' language icon'">
            <p v-else class="null-img">
                {{content.original_language}}
            </p>
        </div>
        <div class="vote">
            <span><strong>Voto: </strong></span>
            <p v-if="content.vote_average != 0">{{content.vote_average}}</p>
            <p v-else>-</p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.card {
    color:black;
    h3, p {
        display: inline;
    }

    .lang {
        img, .null-img {
            height: 1rem;
            display: inline-block !important;
        }
        .null-img {
            width: 1rem;
            height: 1rem;
            background-color: #555;
            font-size: .6rem;
            line-height: 1rem;
            text-align: center;
            border-radius: 50%;
        }
    }
}
</style>