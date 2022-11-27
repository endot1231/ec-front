<script setup lang="ts">
</script>

<template>
  <div class="item">
    <div class="item-image-wrap">
      <PagesItemImage/>
    </div>    
    <div class="item-image-description">
      <PagesItemDescription/>
    </div>  
  </div>
</template>

<style lang="scss" scoped>
.item{
    max-width: 1024px;
    margin: auto;
    display: flex;
    &-image-wrap{
      width: 400px;
    }
    &-image-description{
      flex: 1;
      margin-left: 40px;
    }
}

</style>
