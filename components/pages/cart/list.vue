<template>
  <div>
    <h3 class="title">カート</h3>
    <div class="title-wrap">
      <p class="title-item">商品詳細</p>
      <p class="title-qty">数量</p>
      <p class="title-price">料金</p>
      <p class="title-sum">合計</p>
    </div>
    <ul class="item-list">
      <li class="item" v-for="n in 5">
        <div class="item-detail">
          <div class="item-checkbox">
            <input type="checkbox"/>
          </div>
          <div class="item-img">
            <img src="/img/sample.png"/>
          </div>
          <div class="item-text">
            <h5 class="item-name">アイテムタイトルタイトルアイテムタイトルタイトルアイテムタイトルタイトル</h5>
          </div>
        </div>
        <div class="item-qty">
          <p>1</p>
        </div>
        <p class="item-price">5,000</p>
        <p class="item-sum">5,000</p>
      </li>
    </ul>
  </div>
  
</template>

<style scoped lang="scss">
.title{
  font-size: 24px;
  font-weight: bold;
  margin-bottom: 15px;
  &-wrap{
    border-top: #e5e5e5 1px solid;
    border-bottom:#e5e5e5 1px solid;
    padding: 15px 10px;
    display: flex;
    font-size: 12px;
  }
}

.title,.item{
  &-item{
    width: 508px;
  }
  &-qty,&-price,&-sum{
    width: 80px;
    text-align: center;
  }
}

.item{
  display: flex;
  padding: 15px 10px;
  border-bottom:#e5e5e5 1px solid;  
  &-detail{
    display: flex;
    width: 508px;
  }
  &-checkbox{
    display: flex;
    align-items: center;
    width: 24px;
  }
  &-img{
    width: 100px;
    height: 100px;
    img{
      height: 100%;
      width: 100%;
      object-fit: contain;
    }
  }
  &-text{
    flex: 1;
    margin-left: 18px;
    display: flex;
  }
  &-name{
    font-size: 14px;
    flex: 1;
  }
}
</style>

