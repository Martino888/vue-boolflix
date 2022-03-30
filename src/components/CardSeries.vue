<template>
        <div class="x">
            <img :src="`https://image.tmdb.org/t/p/w342/${src}`" alt="">
            <div>{{ title }}</div>
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
img {
    width: 300px;
    height: 450px;
}

.x{
    width: calc(100% / 3 - 20px);
    padding: 10px;
    justify-content: center;
    text-align: center;
    margin: 10px;
}
</style>
