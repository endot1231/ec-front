<script setup lang="ts">
import { Ref } from "vue";

const PartsIconsStarFilled = resolveComponent("PartsIconsStarFilled")
const PartsIconsStarHalf = resolveComponent('PartsIconsStarHalf')
const PartsIconsStarEmpty = resolveComponent('PartsIconsStarEmpty')

const getComponet = function(status: REVIEW_STATUS) {
  switch(status) {
    case REVIEW_STATUS.Fill:
      return PartsIconsStarFilled;
    case REVIEW_STATUS.Half:
      return PartsIconsStarHalf;
    case REVIEW_STATUS.Empty:
      return PartsIconsStarEmpty;
    default:
      throw new Error("想定外の値が渡されました。"+ " 渡された値:"+ status);
  }
}

const setValue = function(stars: Ref<Array<Object>>,key) {
  REVIEW[key].forEach( (element,index) =>{
    stars.value[index]= element
  });
}

enum REVIEW_STATUS {
  Fill,
  Half,
  Empty,
} 

const REVIEW = {
  ONE_HALF:[REVIEW_STATUS.Half],
  ONE:[REVIEW_STATUS.Fill],
  TWO_HALF:[REVIEW_STATUS.Fill,REVIEW_STATUS.Half],
  TWO:[REVIEW_STATUS.Fill,REVIEW_STATUS.Fill],
  THREE_HALF:[REVIEW_STATUS.Fill,REVIEW_STATUS.Fill,REVIEW_STATUS.Half],
  THREE:[REVIEW_STATUS.Fill,REVIEW_STATUS.Fill,REVIEW_STATUS.Fill],
  FOUR_HALF:[REVIEW_STATUS.Fill,REVIEW_STATUS.Fill,REVIEW_STATUS.Fill,REVIEW_STATUS.Half],
  FOUR:[REVIEW_STATUS.Fill,REVIEW_STATUS.Fill,REVIEW_STATUS.Fill,REVIEW_STATUS.Fill],
  FIVE_HALF:[REVIEW_STATUS.Fill,REVIEW_STATUS.Fill,REVIEW_STATUS.Fill,REVIEW_STATUS.Fill,REVIEW_STATUS.Half],
  FIVE:[REVIEW_STATUS.Fill,REVIEW_STATUS.Fill,REVIEW_STATUS.Fill,REVIEW_STATUS.Fill,REVIEW_STATUS.Fill],
}

let stars = ref([REVIEW_STATUS.Empty,REVIEW_STATUS.Empty,REVIEW_STATUS.Empty,REVIEW_STATUS.Empty,REVIEW_STATUS.Empty])
setValue(stars,"ONE_HALF")

</script>

<template>
  <div class="star-review">
    <component v-for="(start,i) in stars" :key="i" :is="getComponet(start)"></component>
  </div>
</template>

<style lang="scss" scoped>
</style>  