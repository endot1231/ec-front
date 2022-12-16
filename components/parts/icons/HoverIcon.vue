<script setup lang="ts">
const props = defineProps({
  iconPath: {
    type: String,
    required: true
  },
  hoverModalWidth: {
    type: Number,
    default: 300
  },
})

const iconPath = ref(props.iconPath)
let isIconHover = ref(false)

const emit = defineEmits<{
  (event: "clickIcon"): void;
}>();

const clickIcon = () => {
  emit("clickIcon");
};
const hoverIcon = () => {
  isIconHover.value = true
}
const leaveIcon = () =>{
  isIconHover.value = false
}
</script>

<template>
  <div class="icon">
    <img @click="clickIcon" @mouseover="hoverIcon" @mouseleave="leaveIcon" :src="iconPath" wdith="26" height="26">
    <div v-show="isIconHover" class="icon-hover-content" :class="{'hover' : isIconHover}" @mouseover="hoverIcon" @mouseleave="leaveIcon">
      <slot />
    </div>
  </div>
</template>

<style scoped lang="scss">
.icon{
  position: relative;
  border-radius: 5px;
  cursor: pointer;
  padding: 4px;
  &-hover-content{
    position: absolute;
    z-index: 2;
    visibility: hidden;
    &.hover{
      visibility: visible;
      animation-duration: 0.3s;
      animation-name: fade-in;
    }
  }
}

@keyframes fade-in {
  0% {
    visibility: hidden;
    opacity: 0;
  }

  50% {
    visibility: visible;
    opacity: 0.5;
  }

  100% {
    visibility: visible;
    opacity: 1;
  }
}
</style>
