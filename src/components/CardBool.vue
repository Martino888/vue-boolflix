<template>
    <div class=" x flip-card">
        <div class="flip-card-inner">
            <div class="flip-card-front">
                <img class="img-fluid"  :src="`https://image.tmdb.org/t/p/w342/${src}`"  alt="title">
            </div>
            <div  >
                <h3 class="fw-bold">Titolo:{{ title }}</h3>
                <p>Titolo originale:{{origianlTitle }}</p>
                <lang-flag :iso="lang" :squared="false" />
                <h4>vote:{{ vote }}</h4>
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

    }
}
</script>

<style lang="scss" scoped>

    img {
        width: 300px;
        height: 450px;
        border: 3px solid rgb(206, 192, 192);
    }

.x{
    width: calc(100% / 3 - 20px);
    padding: 10px;
    justify-content: center;
    text-align: center;
    margin: 10px;
}


.flip-card {
    background-color: blue;
    border: 1px solid black;
    width: 300px;
    height: 470px;
    perspective: 1000px;
}

.flip-card-front, .flip-card-back {
    position: absolute;
    width: 100%;
    height: 100%;
    -webkit-backface-visibility: hidden;
    backface-visibility: hidden;
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



</style>
