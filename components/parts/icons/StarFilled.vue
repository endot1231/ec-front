<script setup lang="ts">
import { defineProps } from 'vue';

const props = defineProps({
  width: {
    type: Number,
    default: 16
  },
  height: {
    type: Number,
    default: 16
  }
})

const width = ref(props.width)
const height = ref(props.height)
</script>

<template>
  <div class="star-filled">
    <svg fillrule="evenodd" viewBox="0 0 24 24" :width="width" :height="height">
      <path class="cls-1"
        d="M22,9.69a.72.72,0,0,0-.57-.48l-6.06-.88L12.63,2.86a.73.73,0,0,0-1.26,0L8.66,8.33,2.6,9.21A.72.72,0,0,0,2,9.69a.69.69,0,0,0,.18.71L6.6,14.66l-1,6a.71.71,0,0,0,.28.69.73.73,0,0,0,.74.05L12,18.58l5.42,2.84a.72.72,0,0,0,.74-.05.71.71,0,0,0,.28-.69l-1-6,4.39-4.26A.69.69,0,0,0,22,9.69Z">
      </path>
    </svg>
  </div>
</template>

<style lang="scss" scoped>
.star-filled {
  display: inline-block;
}

svg {
  fill: #ffb818;
}
</style>  