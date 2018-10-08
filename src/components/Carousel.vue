<template>
  <div class='carousel-wrap'>
      <transition-group
        name='carousel'
        class='carousel'
        tag="div">
        <div
          v-for="(slide) in slides" 
          class='slide'
          :key="slide.id">
          <img class='slide__image' :src='slide.img'>
        </div>
      </transition-group>
      <div class='carousel-nav'>
        <button class='carousel-nav__button' @click="moveCarousel(-1)">prev</button>
        <button class='carousel-nav__button' @click="moveCarousel(1)">next</button>
      </div>
    </div>
</template>

<script>

export default {
  name: 'Carousel',
  data: function () {
    const slides = []
    const numberOfSlides = 9   // should to be an odd

    for(let slide = 0; slide < numberOfSlides; slide++ ) {
      slides.push({img:`https://cataas.com/cat/says/${slide}?width=200&height=200`, id: slide+1})
    }
    return {
      slides
    }
  },
  methods: {
    moveCarousel (direction) {
      if (direction === 1) {
        const first = this.slides.shift()
        this.slides = this.slides.concat(first)
      } else if (direction === -1) {
        const last = this.slides.pop()
        this.slides = [last].concat(this.slides)
      }
    }
  }
}
</script>

<style>
@import "./Carousel.css"
</style>
