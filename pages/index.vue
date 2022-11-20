<template>
  <div class="index-page">
    <div class="sidebar-wrap">
      <LayoutsSidebar/>
    </div>
    <div class="item-list-wrap">
      <PagesIndexItemList/>
    </div>
  </div>
</template>

<style scoped lang="scss">
.index-page{
  display: flex;
}
.sidebar-wrap{
  width: 230px;
  padding: 10px;
}

.item-list-wrap{
  margin-left: 20px;
  max-width: 1200px;
  flex: 1;
}
</style>

