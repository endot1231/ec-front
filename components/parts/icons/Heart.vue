<script setup lang="ts">
const emit = defineEmits<{
  (event: "clickIcon"): void;
}>();

const clickIcon = () => {
  emit("clickIcon");
};
</script>

<template>
  <div class="icon">
    <img @click="clickIcon" src="~/assets/image/icon/heart.svg" wdith="26" height="26">
  </div>
</template>

<style lang="scss">
.icon{
  border-radius: 5px;
}
</style>
