<template>
  <div id="app">
    <Header/>
    <Carousel/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Carousel from './components/Carousel.vue'

export default {
  name: 'app',
  components: {
    Header, Carousel
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  height: 100%;
}
body, html {
  margin: 0;
  #f4fff3
  font-family: "Comic Sans MS", cursive, sans-serif;
}
</style>
