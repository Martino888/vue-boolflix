<template>
    <div class="container">
        <div class="row col-3 card">
            <b>{{ title }}</b>
            <p>{{origianlTitle }}</p>
            <lang-flag :iso="lang" :squared="false" />
            <h4>{{ vote }}</h4>
        </div>
    </div>
</template>

<script>
import LangFlag from 'vue-lang-code-flags';

export default {
    name: 'CardBool',
    props: {
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
.card{
    width: calc(100% / 5 - 20px);
    min-width: 150px;
    background-color: rgb(37, 101, 170);
    padding: 10px;
    justify-content: center;
    text-align: center;
    margin: 10px;
}
</style>
