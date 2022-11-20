<script setup lang="ts">
import { ref } from "vue";

let isFocus = ref(false);
const clickTextArea =() =>{
  isFocus.value = true
}
const unClickTextArea =() =>{
  isFocus.value = false
}
let itemList = ["みかん","りんご","ばなな","もも"]

const clickResult =() =>{
  console.log("aaaaaaaaaaaaaaaaa")
}

</script>

<template>
  <div class="serachbar">
    <div>
      <input class="serachbar-text" type="text" @click="clickTextArea" @blur="unClickTextArea" placeholder="何をお探しですか？"/>
    </div>
    <div class="result" v-if="isFocus">
      <ul class="result-list">
        <li class="result-item" v-for="item in itemList" @click="clickResult">{{item}}</li>
      </ul>
    </div>
  </div>

</template>

<style lang="scss" scoped>
.serachbar{
  display: block;
  position: relative;
  width: 100%;
  text-decoration: none;
  &-text{
    padding: 10px 16px;
    width: 100%;
    border: #e5e5e5 1px solid;
    &:focus{
      outline: none;
    }
  }
  input{
    box-sizing: border-box;
  }
}

.result{
  position: absolute;
  box-sizing: border-box;
  z-index: 3;
  left: 0;
  width: calc(100%);
  border-radius: 10px;
  &-list{
    width: 100%;
  }
  &-item{
    box-sizing: border-box;
    width: 100%;
    padding: 10px 16px;
    background-color: white;
    cursor: pointer;
    border-right: solid 1px #e5e5e5;
    border-left: solid 1px #e5e5e5;
    &:hover{
      background-color: #e5e5e5;
    }
    &:last-child{
      border-bottom: solid 1px #e5e5e5;
      border-radius: 0px 0px 5px 5px;
    }
  }
}

</style>  