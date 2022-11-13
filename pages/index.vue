<template>
  <div class="index-page">
    <div class="sidebar-wrap">
      <OrganismsSidebar/>
    </div>
    <div class="item-list-wrap">
      <OrganismsItemList/>
    </div>
  </div>
</template>

<style scoped lang="scss">
.index-page{
  display: flex;
}
.sidebar-wrap{
  width: 190px;
}

.item-list-wrap{
  width: 834px;
}
</style>

