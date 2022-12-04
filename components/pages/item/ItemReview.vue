<template>
  <div>
    <h2 class="page-title">商品レビュー</h2>
    <div class="item">
      <div class="item-image">
        <img src="/img/sample.png" />
      </div>
      <div class="item-text">
        <h1 class="item-name">サンプルサンプルサンプル</h1>
        <p class="item-price">\4,0000</p>
        <nuxt-link class="shop-name" to="shop/1"><img src="~/assets/image/icon/shop.svg" />ショップ名</nuxt-link>
      </div>
    </div>
    
    <div class="review">
      <p class="review-title">総合評価</p>
      <div class="review-content-wrap">
        <div class="review-star">
          <p class="review-average">4.0</p>
          <UiStarReview class="review-stars" :star-height="28" :star-width="28"/>
          <p class="review-total">100件</p>
        </div>
        <div class="review-counts">
          <ul class="review-list">
            <li class="review-item">
              <span class="review-point">星5</span>
              <span class="review-bar">
                <span class="review-bar-inner"></span>
              </span>
              <span class="review-count">50件</span>
            </li>
            <li class="review-item">
              <span class="review-point">星4</span>
              <span class="review-bar">
                <span class="review-bar-inner"></span>
              </span>
              <span class="review-count">40件</span>
            </li>
            <li class="review-item">
              <span class="review-point">星3</span>
              <span class="review-bar">
                <span class="review-bar-inner"></span>
              </span>
              <span class="review-count">30件</span>
            </li>
            <li class="review-item">
              <span class="review-point">星2</span>
              <span class="review-bar">
                <span class="review-bar-inner"></span>
              </span>
              <span class="review-count">20件</span>
            </li>
            <li class="review-item">
              <span class="review-point">星1</span>
              <span class="review-bar">
                <span class="review-bar-inner"></span>
              </span>
              <span class="review-count">10件</span>
            </li>
          </ul>
        </div>
      </div>
    </div>

    <div class="comment">
      <p class="comment-title">すべてのレビュー</p>
      <ul class="comment-list">
        <li class="comment-item">
          <p class="comment-item-title">レビュータイトル</p>
          <UiStarReview/>
          <p class="comment-item-contetn">内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容</p>
        </li>

        <li class="comment-item">
          <p class="comment-item-title">レビュータイトル</p>
          <UiStarReview/>
          <p class="comment-item-contetn">内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容</p>
        </li>

        <li class="comment-item">
          <p class="comment-item-title">レビュータイトル</p>
          <UiStarReview/>
          <p class="comment-item-contetn">内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容内容</p>
        </li>
      </ul>
    </div>

  </div>
</template>
  
<style scoped lang="scss">

.page-title{
  font-size: 28px;
  font-weight: bold;
  padding-bottom: calc(10px - 0.1em);
  border-bottom: 1px solid #ccc;
}

.shop-name {
  display: flex;
  align-items: center;
  font-size: 14px;
  color: #007185;
  margin-top: 8px;
  img {
    width: 30px;
    height: 30px;
  }
}

.item {
  display: flex;
  border-bottom: 8px solid #eaeaea;
  padding-bottom: 5px;
  &-name {
    font-size: 24px;
    margin-top: 15px;
  }

  &-text {
    padding-left: 24px;
  }
  &-price{
    margin-top: 8px;
    font-size: 20px;
    color: #c00;
  }

  &-image {
    img {
      object-fit: contain;
      width: 131px;
      height: 131px;
    }
  }
}

.review{
  margin-top: 40px;
  padding-left: 20px;
  padding-bottom: 30px;
  border-bottom: 8px solid #eaeaea;
  &-title{
    font-weight: 700;
    font-size: 16px;
  }
  &-content-wrap{
    display: flex;
    margin-top: 20px;
    align-items: center;
  }
  &-star{
    display: flex;
    flex-direction: column;
    text-align: center;
  }
  &-stars{
    margin-top: 10px;
  }
  &-counts{
    margin-left: 40px;
  }
  &-average{
    font-size: 28px;
    text-align: center;
    font-weight: bold;
  }
  &-total{
    margin-top: 10px;
  }
  &-bar{
    height: 6px;
    background-color: #f5f5f5;
    width: 100px;
    display: inline-block;
    margin-left: 6px;
    &-inner{
      background-color: grey;
      display: inline-block;
    }
  }
  &-count{
    margin-left: 10px;
    font-size: 14px;
    color: #04c;
  }
  &-point{
    font-size: 14px;
    color: #333;
  }
  &-item{
    display: flex;
    align-items: center;
    margin-top: 15px;
  }
}

.comment{
  margin-top: 40px;
  &-title{
    font-size: 20px;
    font-weight: 700;
  }
  &-list{
    margin-top: 20px;
  }
  &-item{
    border: 1px solid #eaeaea;
    border-radius: 10px;
    margin-bottom: 10px;
    padding: 20px;
  }
}

</style>