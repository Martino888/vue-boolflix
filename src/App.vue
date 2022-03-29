<template>
  <div id="app">
    <HeaderBool></HeaderBool>
    <MainBool></MainBool>
  </div>
</template>

<script>

import HeaderBool from './components/HeaderBool.vue'
import MainBool from './components/MainBool.vue'
export default {
  name: 'App',
  components: {
    HeaderBool,
    MainBool,
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html {
  background-color: gray;
}
@import "~bootstrap/scss/bootstrap";
</style>
