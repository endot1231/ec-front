<template>
<div class="item-description">
  <nuxt-link to="shop/1" class="shop-name"><img src="~/assets/image/icon/shop.svg"/>テストショップ名</nuxt-link>
  <h1 class="item-name">商品名商品名商品名商品名商品名商品名</h1>
  <div class="item-review">
    <UiStarReview />
    <nuxt-link to="/item/1" class="item-review-link">4.0</nuxt-link>
  </div>
  <div class="item-detail">
    テストテストテストテストテストテストテストテストテストテストテストテスト
    テストテストテストテストテストテストテストテストテストテストテストテスト
    テストテストテストテストテストテストテストテストテストテストテストテスト
    テストテストテストテストテストテストテストテストテストテストテストテスト
  </div>

  <div class="category">
    <ul class="category-list">
      <li class="category-item">
        <div class="category-title">
          <p class="category-text">色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ</p>
          <p class="stock">在庫あり</p>
        </div>
        <div class="cart-button">カートに入れる</div>
      </li>

      <li class="category-item">
        <div class="category-title">
          <p class="category-text">色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ</p>
          <p class="stock">在庫あり</p>
        </div>
        <div class="cart-button">カートに入れる</div>
      </li>

      <li class="category-item">
        <div class="category-title">
          <p class="category-text">色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ色 / サイズ</p>
          <p class="stock">在庫あり</p>
        </div>
        <div class="cart-button">カートに入れる</div>
      </li>
    </ul>
  </div>
</div>
</template>

<style scoped lang="scss">
.shop-name{
  display: flex;
  align-items: center;
  font-size: 14px;
  color: #007185;
  img{
    width: 30px;
    height: 30px;
  }
}
.item{
  &-name{
    font-size: 24px;
    margin-top: 15px;
  }
  &-review{
    display: flex;
    margin-top: 5px;
  }
  &-detail{
    margin-top: 10px;
    border-top: 1px #eee solid;
    padding: 10px;
  }
}

.category{
  margin-top: 10px;
  &-item{
    border-top: 1px #eee solid;
    padding: 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 60px;
  }
  &-text{
    font-size: 12px;
  }
}

.stock{
  margin-top: 5px;
  font-size: 12px;
}

.cart-button{
  width: 170px;
  background-color: #252525;
  color: #ffffff;
  padding: 11px 15px;
  cursor: pointer;
  &:hover{
    opacity: 0.8;
  }
}
</style>