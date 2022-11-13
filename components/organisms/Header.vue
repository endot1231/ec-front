<template>
  <header class="header">
    <div class="header-wrap">
      <div class="serach-bar-wrap">
        <MoleculesSearchBar/>
      </div>
      <div class="icon-list">
        <MoleculesIconList/>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.header{
  &-wrap{
    margin: auto;
    display: flex;
    justify-content: space-between;
  }
}

.serach-bar-wrap{
  width: 490px;
}
.icon-list{
  display: flex;
  align-items: center;
}
</style>