<template>
        <div class="x">
            <img :src="`https://image.tmdb.org/t/p/w342${src}`" alt="">
            <b>{{ title }}</b>
            <p>{{origianlTitle }}</p>
            <lang-flag :iso="lang" :squared="false" />
            <h4>{{ vote }}</h4>
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
        vote: Number,
    },
    components: {
        LangFlag
    },
}
</script>

<style lang="scss" scoped>
.x{
    display: inline-block;
    width: calc(100% / 5 - 20px);
    min-width: 150px;
    background-color: rgb(37, 101, 170);
    padding: 10px;
    justify-content: center;
    text-align: center;
    margin: 10px;
}
</style>
