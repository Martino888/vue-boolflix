<template>
    <div class=" x flip-card">
        <div class="flip-card-inner">
            <div class="flip-card-front">
                <img class="img-fluid"  :src="`https://image.tmdb.org/t/p/w342/${src}`"  alt="title">
            </div>
            <div class="flip-card-back" >
                <h3 class="fw-bold">Titolo:{{ title }}</h3>
                <p>Titolo originale:{{origianlTitle }}</p>
                <lang-flag :iso="lang" :squared="false" />
                <div>
                    <strong> vote : </strong>
                    <strong v-for="(element, index) in 5 " :key="index" :class="index < votoIntero(vote) ? 'yellows' :  '' " >&starf; </strong>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import LangFlag from 'vue-lang-code-flags';

export default {
    name: 'CardBool',
    props: {
        src: String,
        title: String,
        origianlTitle: String,
        lang: String,
        vote:  Number,
    },
    components: {
        LangFlag
    },
    methods: {
        votoIntero(voto) {
            return Math.ceil(voto / 2);
        }
    }
}
</script>

<style lang="scss" scoped>

    img {
        width: 300px;
        height: 450px;
        border: 3px solid rgb(206, 192, 192);
    }

    .yellows {
        color:yellow;
    }

.x{
    width: calc(100% / 3 - 20px);
    padding: 10px;
    justify-content: center;
    text-align: center;
    margin: 10px;
}


.flip-card {
    width: 300px;
    height: 470px;
    perspective: 1000px;
}

.flip-card-front {
    position: absolute;
    width: 100%;
    height: 100%;
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
    z-index: 1;
}

.flip-card-back{
    background: rgb(156, 74, 74);
    transform: rotateY(180deg);
    z-index: 0;
    width: 100%;
    height: 100%;
}

.flip-card-inner {
    position: relative;
    width: 100%;
    height: 100%;
    text-align: center;
    transition: transform 0.8s;
    transform-style: preserve-3d;
}

.flip-card:hover .flip-card-inner {
    transform: rotateY(180deg);
}

.flip-card:hover .flip-card-back {
    z-index: 0;
}

</style>
