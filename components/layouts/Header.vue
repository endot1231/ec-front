<script setup lang="ts">
function clickHeart(event): void {
    navigateTo('/')
}

function clickBell(event): void {
    navigateTo('/')
}

function clickCart(event): void {
    navigateTo('/')
}
</script>


<template>
  <header class="header">
    <div class="header-wrap">
      <div class="serach-bar-wrap">
        <img class="header-icon" src="~/assets/image/icon/header.png"/>
        <PartsSearchBar/>
      </div>
      <div class="icon-list">
        <PartsIconsHoverIcon @clickIcon="clickHeart" icon-path="/img/cart.svg">
          <div class="hover-content" >
            <h4 class="hover-title">カート</h4>
            <ul class="hover-list">
              <li class="hover-item" v-for="n in 5">
                <a class="hover-link" href="/test">アイテムアイテムアイテムアイテムアイテムアイテムアイテム
                アイテムアイテムアイテムアイテムアイテム</a>
              </li>
            </ul>
            <div class="hover-show-all">
              <nuxt-link to="/cart">すべて表示</nuxt-link>
            </div>
          </div>    
        </PartsIconsHoverIcon>

        <PartsIconsHoverIcon @clickIcon="clickHeart" icon-path="/img/heart.svg">
          <div class="hover-content" >
            <h4 class="hover-title">お気に入り</h4>
            <ul class="hover-list">
              <li class="hover-item" v-for="n in 5">
                <a class="hover-link" href="/test">アイテムアイテムアイテムアイテムアイテムアイテムアイテム
                アイテムアイテムアイテムアイテムアイテム</a>
              </li>
            </ul>
            <div class="hover-show-all">
              <nuxt-link to="/favorite">すべて表示</nuxt-link>
            </div>
          </div>    
        </PartsIconsHoverIcon>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.header{
  width: 100%;
  padding-top: 10px;
  padding-bottom: 10px;
  border-bottom: 1px solid #e5e5e5;
  &-wrap{
    max-width: 1024px;
    margin: auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  &-icon{
    width: 40px;
    height: 100%;
    margin-right: 20px;
    align-items: center;
  }
}

.serach-bar-wrap{
  width: 490px;
  display: flex;
}

.icon-list {
  display: flex;
  column-gap: 10px;
}

.hover{
  &-content{
    position: absolute;
    width: 250px;
    padding: 25px 20px;
    top: -3px;
    right: -155px;
    background-color: #fff;
    border-radius: 8px;
    border: #e5e5e5 1px solid;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.08);
  }
  &-title{
    text-align: center;
    margin-bottom: 25px;
    font-weight: 600;
  }
  &-list{
    display: flex;
    flex-direction: column;
    row-gap: 10px;
  }
  &-item{
    &:hover{
      text-decoration: underline;
      opacity: 0.8;
    }
  }
  &-link{
    line-height: 1;
    font-size: 12px;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 2;
    overflow: hidden;
  }
  &-show-all{
    margin-top: 15px;
    text-align: center;
    a {
      font-size: 12px;
      color: rgb(35, 171, 221);
      &:hover{
        text-decoration: underline;
      }
    }
  }
}
</style>