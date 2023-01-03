<template>
  <div class="order">
    <h3 class="order-title">注文合計</h3>
    <div class="order-count">
      <p class="order-count-title">商品数</p>
      <p class="order-count-number">1</p>
    </div>
    <div class="order-summary">
      <p class="order-summary-title">合計</p>
      <p class="order-summary-number">\1,700</p>
    </div>
    <button class="order-button">注文画面に進む</button>
  </div>
</template>

<style scoped lang="scss">
.order {
  background-color: #EFEFEF;
  padding: 20px;
  &-title {
    padding: 15px 0px;
    border-bottom: #E4E4E4 1px solid;
    font-weight: bold;
  }
  &-count, &-summary {
    padding: 15px 0px;
    display: flex;
    justify-content: space-between;
    font-size: 14px;
  }
  &-button {
    width: 100%;
    padding: 8px 0px;
    text-align: center;
    background-color: #323232;
    border: 0px;
    color: #D5D5D5;
    cursor: pointer;
    &:hover {
      opacity: 0.8;
    }
  }
}
</style>

