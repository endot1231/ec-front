<script setup lang="ts">
import { ref } from "vue";
import { onBeforeRouteLeave, onBeforeRouteUpdate } from 'vue-router'

type Category = {
  name: string
  id: number
  parentId: number
  childrenId: number
}

const category1: Category = {
  name: "カテゴリ1",
  id: 1,
  parentId: null,
  childrenId: 4
}

const category2: Category = {
  name: "カテゴリ2",
  id: 2,
  parentId: null,
  childrenId: null
} 

const category3: Category = {
  name: "カテゴリ3",
  id: 1,
  parentId: null,
  childrenId: null
}

const category4: Category = {
  name: "カテゴリ4",
  id: 4,
  parentId: 1,
  childrenId: null
} 

let categoryArray = ref([category1,category2,category3,category4])
let categoryName = ref("すべて")
let selectedCategory = ref(-1)

const serachedCategory = computed(() => {
  if(selectedCategory.value == -1){
    return categoryArray.value.filter((category) => category.parentId == null);
  }else{
    return categoryArray.value.filter((category) => category.parentId == selectedCategory.value);
  }
})

const categoryClick = (category: Category) =>{
  if(category.childrenId == null){
    navigateTo(`/serach?category_id=${category.id}`);
  }else{
    selectedCategory.value = category.id
    categoryName.value = category.name
    navigateTo(`?category_id=${category.id}`);
  }
}

onBeforeRouteUpdate(async (to, from) => {
  if (to.query["category_id"]){
    let category = categoryArray.value.find((category) => category.id == Number(to.query["category_id"]))
    selectedCategory.value = category.id
    categoryName.value = category.name
  }else{
    selectedCategory.value = -1
    categoryName.value = "すべて"
  }
})
</script>

<template>
  <div class="sitedebar">
    <h3 class="title">カテゴリから探す</h3>
    <div class="search-bar">
      <PartsSearchBar/>
    </div>
    <p class="category-title">{{categoryName}}</p>
    <ul class="category-list" >
      <li v-for="category in serachedCategory" :key="category.id">
        <nuxt-link class="category-item" @click.native="categoryClick(category)">
          <span>{{category.name}}</span>
          <svg fillrule="evenodd" viewBox="0 0 24 24" class="icon primary" width="16" height="16">
            <path class="cls-1" d="M9.93,2.29a1,1,0,0,0-1.41,0,1,1,0,0,0,0,1.42l8,8a.41.41,0,0,1,0,.58l-8,8a1,1,0,0,0,1.41,1.42l8-8a2.43,2.43,0,0,0,0-3.42Z">     
            </path>
          </svg>
        </nuxt-link>
      </li>
    </ul> 
  </div>
</template>

<style scoped lang="scss">
.sitedebar {
  width: 100%;
}
.title{
  font-size: 14px;
  padding-bottom: 10px;
}
.search-bar{
  width: 100%;
  padding-bottom: 20px;
}
.category{
  &-title{
    padding-bottom: 10px;
  }
  &-item{
    padding: 10px 5px;
    width: 100%;
    display: flex;
    justify-content: space-between;
    &:hover{
      background-color: #e5e5e5;
    }
    a{
      width: 100%;
      display: flex;
      justify-content: space-between;
    }
  }
}
</style>
