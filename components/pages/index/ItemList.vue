<script setup lang="ts">
function clickItem(item_id): void {
  navigateTo('`/item/item_id')
}
</script>

<template>
  <div class="item-list">
    <div class="item-card-wrap" v-for="n in 8">
      <UiItemCard />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.item-list {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

.item-card-wrap {
  width: calc(25% - 22px);
}

@media screen and (max-width: 1024px) {
  .item-card-wrap {
    width: calc(33% - 22px);
  }
}

@media screen and (max-width: 768px) {
  .item-card-wrap {
    width: 100%
  }
}
</style>