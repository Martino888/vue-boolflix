<template>
    <main class="bg-primary">
        <div class="container">
            <h1 v-show="arrMovies != ''" >Movie</h1>
            <div class="row col d-flex justify-content-center">
                    <CardBool v-for="element in arrMovies" :key="element.id"
                    :src="element.poster_path"
                    :title="element.title"
                    :origianlTitle="element.original_title"
                    :lang="element.original_language"
                    :vote="element.vote_average"
                    />
            </div>
            <h1 v-show="arrSeries != ''" >Serie tv</h1>
            <div class="row col d-flex justify-content-center">
                    <CardSeries v-for="element in arrSeries" :key="element.id"
                    :src="element.poster_path"
                    :title="element.name"
                    :origianlTitle="element.original_name"
                    :lang="element.original_language"
                    :vote="element.vote_average"
                    />
            </div>
        </div>
    </main>
</template>

<script>
import CardSeries from './CardSeries.vue'
import CardBool from './CardBool.vue'
export default {
    name: 'MainBool',
    components:{
            CardBool,
            CardSeries
        },
    props: {
        arrMovies: Array,
        arrSeries: Array
    },
}
</script>

<style scoped lang="scss">
main{
min-height:calc(100vh - 60px) ;
}

</style>
