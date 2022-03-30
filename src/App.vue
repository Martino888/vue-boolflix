<template>
  <div id="app">
    <HeaderBool @callSearch="callingSearch"></HeaderBool>
    <MainBool :arrMovies="arrMovies"></MainBool>
  </div>
</template>

<script>
import axios from "axios"
import HeaderBool from './components/HeaderBool.vue'
import MainBool from './components/MainBool.vue'
export default {
  name: 'App',
  components: {
    HeaderBool,
    MainBool,
  },
  data(){
    return {
      arrMovies: []
    }
  },
  methods: {
    callingSearch(inputMovie){
      axios.get('https://api.themoviedb.org/3/search/movie?api_key=2a1eafb77e5173892c5f55c2d7d7a8c8&page=1&include_adult=false&language=en-US&query='+inputMovie)
      .then((rispostaMovie) =>{
        console.log(rispostaMovie)
        this.arrMovies = rispostaMovie.data.results
      })
    }
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

$primary: rgb(139, 139, 139);

@import "~bootstrap/scss/bootstrap";
</style>
