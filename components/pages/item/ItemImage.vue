<script setup lang="ts">
import {ref} from 'vue'
import 'vue3-carousel/dist/carousel.css'
import { Carousel, Slide, Navigation } from 'vue3-carousel'
const images = ref(["/img/sample.png", "/img/sample1.png", "/img/sample2.png", "/img/sample3.png"])
let currentSlide = ref(0)
function slideTo(value: number): void {
  currentSlide.value = value
}
</script>

<template>
  <div class="item-image">
    <Carousel id="gallery" :items-to-show="1" :wrap-around="false" v-model="currentSlide">
      <Slide  v-for="slide in images" :key="slide">
        <div class="carousel__item"><img :src="slide"/></div>
      </Slide>
      <template #addons>
        <Navigation />
      </template>
    </Carousel>

    <Carousel id="thumbnails" :items-to-show="4" :wrap-around="true" v-model="currentSlide" snapAlign="start" >
      <Slide  v-for="(slide,index) in images" :key="slide">
        <div class="carousel__item" @click.prevent="slideTo(index)"><img :src="slide"/></div>
      </Slide>
    </Carousel>
  </div>
</template>

<style scoped lang="scss">

.carousel__item {
  height: 300px;
  width: 100%;
  background-color: #e5e5e5;
  color: var(--vc-clr-white);
  font-size: 20px;
  border-radius: 8px;
  display: flex;
  justify-content: center;
  align-items: center;
  img{
    position: absolute;
    height: calc(100% - 10px);
    width: calc(100% - 10px);
    object-fit: contain;
  }
}
#thumbnails{
  .carousel__item{
    height: 100px;
    position: relative;
  }
  .carousel__slide {
    padding: 10px;
    &--active{
      .carousel__item{
        border: 1px gray solid;
      }
    }
  }
}

#gallery{
  .carousel__slide {
    padding: 0px 10px 10px 10px;
  }
}
</style>