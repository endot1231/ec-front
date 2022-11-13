<script setup lang="ts">
const emit = defineEmits<{
  (event: "clickItem",item_id: number): void;
}>();

const clickItem = (item_id: number) => {
  emit("clickItem",item_id);
};
</script>

<template>
    <nuxt-link to="/item/1" class="item-card">
        <div class="item-image">
            <img src="/img/sample.png"/>
        </div>
        <div class="item-text">
            <p class="item-title">イラスト</p>
            <p class="item-review">4.0</p>
            <p class="item-price">4000円</p>
        </div>
    </nuxt-link>
</template>

<style lang="scss" scoped>
.item-card{
    background: red;
    display: block;
    width: 190px;
    height: 300px;
    padding: 5px;
    text-decoration: none;
}

.item-image{
    img{
        height: 150px;
        width: 100%;
        object-fit: cover;
    }
}
</style>