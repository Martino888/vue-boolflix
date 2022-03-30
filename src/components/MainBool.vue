<template>
    <main class="bg-primary">
        <div class="container">
            <h1>Movie</h1>
            <div class="row col">
                <div class="card">
                    <CardBool v-for="element in arrMovies" :key="element.id"
                    :title="element.title"
                    :origianlTitle="element.original_title"
                    :lang="element.original_language"
                    :vote="element.vote_average"
                    />
                </div>
            </div>
        </div>
    </main>
</template>

<script>
import CardBool from './CardBool.vue'
export default {
    name: 'MainBool',
    components:{
            CardBool
        },
    props: {
        arrMovies: Array
    }
}
</script>

<style scoped lang="scss">
main{
min-height:calc(100vh - 60px) ;
}
</style>
