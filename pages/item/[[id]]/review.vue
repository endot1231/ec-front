<script setup lang="ts">
</script>

<template>
  <div class="review">
    <PagesItemReview/>
  </div>
</template>

<style lang="scss" scoped>
.review{
    max-width: 1024px;
    margin: auto;
    &-image-wrap{
    display: flex;
      width: 400px;
    }
    &-image-description{
      flex: 1;
      margin-left: 40px;
    }
}

</style>
