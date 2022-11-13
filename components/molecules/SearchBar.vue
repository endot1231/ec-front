<template>
  <div class="serach-bar">
    <input type="text" v-model="input" placeholder="なにをお探しですか？" @focus="onFocus" @blur="blur" />
    <div class="suggestion">
      <ul class="suggestion-list" v-if="isInputFoucs">
        <li class="item fruit" v-for="fruit in filteredList()" :key="fruit">
          {{ fruit }}
        </li>
      </ul>
      <div class="item error" v-if="input && !filteredList().length">
        {{ input }}
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
let input = ref("");
const fruits = ["apple", "banana", "orange"];
const isInputFoucs = ref(false);

function filteredList() {
  return fruits.filter((fruit) =>
    fruit.toLowerCase().includes(input.value.toLowerCase())
  );
}
function onFocus() {
  isInputFoucs.value = true;
}
function blur() {
  isInputFoucs.value = false;
}
</script>

<style lang="scss">
input {
  display: block;
  width: 100%;
  padding: 10px 0px 10px 10px;
  background: white url("assets/search-icon.svg") no-repeat 15px center;
  background-size: 15px 15px;
  font-size: 16px;
  border: none;
  border-radius: 5px;
  box-shadow: rgba(50, 50, 93, 0.25) 0px 2px 5px -1px,
    rgba(0, 0, 0, 0.3) 0px 1px 3px -1px;
}

.suggestion {
  border: 1px solid #20212419;
  border-radius: 5px;
  position: relative;
  &-list{
    position: absolute;
    background: white;
    width: 100%;
    border: 1px solid #20212419;
  }
}

.item {
  padding: 10px 10px;
  cursor: pointer;

  &:hover {
    background: #20212419;
  }
}
</style>
