<template>
  <div class="cart-page">
    <div class="item-list">
      <PagesCartList/>
    </div>
    <div class="summary">
      <PagesCartOrder/>
    </div>
  </div>
</template>

<style scoped lang="scss">
.cart-page{
  margin: auto;
  max-width: 1024px;
  display: flex;
}
.item-list{
  width: calc(100% - 266px);
}

.summary{
  margin-top: 84px;
  margin-left: 16px;
  width: 250px;
}
</style>

