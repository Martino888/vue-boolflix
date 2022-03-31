<template>
        <div class="x">
            <img class="img-fluid" :src="`https://image.tmdb.org/t/p/w342/${src}`" alt="title">
            <div class="y">
                <div class="fw-bold">Titolo:{{ title }}</div>
                <p>Titolo originale:{{origianlTitle }}</p>
                <lang-flag :iso="lang" :squared="false" />
                <h4>vote:{{ vote }}</h4>
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
}
</script>

<style lang="scss" scoped>

    img {
        width: 300px;
        height: 450px;
        border: 3px solid rgb(206, 192, 192);
    }

img:hover {
    display: none;
}

.x{
    width: calc(100% / 3 - 20px);
    padding: 10px;
    justify-content: center;
    text-align: center;
    margin: 10px;
}
</style>
