<template>
  <div class="shop">
    <div class="shop-desc">
      <img class="shop-img" src="/img/sample.png">
      <div class="shop-text-wrap">
        <p class="shop-name">ショップ名ショップ名</p>
        <p class="shop-kana">しょっぷめいしょっぷめい</p>
        <p class="shop-content">説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明
          説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明
          説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明
          説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明説明
        </p>
      </div>
    </div>

    <p class="item-title">商品一覧</p>
    <div class="item-list">
      <div class="item-card-wrap" v-for="n in 8">
        <UiItemCard />
      </div>
    </div>

  </div>
</template>

<style lang="scss" scoped>
.shop {
  max-width: 1024px;
  margin: auto;

  &-img {
    width: 300px;
    height: 300px;
    object-fit: contain;
    box-shadow: 0 10px 20px 0 rgb(0 0 0 / 10%);
    border-radius: 16px;
  }

  &-desc {
    display: flex;
    margin-bottom: 80px;
    padding-bottom: 30px;
    border-bottom: #e5e5e5 1px solid;
  }

  &-text {
    &-wrap {
      margin-left: 40px;
    }
  }

  &-name {
    font-size: 30px;
    font-weight: 600;
    margin-top: 20px;
  }

  &-kana {
    font-size: 13px;
    line-height: 1;
    margin-top: 15px;
  }

  &-content {
    margin-top: 45px;
    line-height: 1.84615;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 2;
    overflow: hidden;
    text-overflow: ellipsis;
    word-break: break-word;
    word-wrap: normal;
    font-weight: 600;
  }
}

.item-title{
  font-size: 20px;
  font-weight: 600;
  margin-bottom: 20px;
}
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
