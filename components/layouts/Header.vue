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
        <PartsIconsHeart @clickIcon="clickHeart" />
        <PartsIconsBell @clickIcon="clickBell" />
        <PartsIconsCart @clickIcon="clickCart" />
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
</style>