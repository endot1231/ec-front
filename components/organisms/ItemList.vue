<script setup lang="ts">
function clickItem(item_id): void {
    navigateTo('`/item/item_id')
}
</script>

<template>
    <div class="item-list">
        <div v-for="n of 8" :key="n">
            <MoleculesItemCard @click-item="clickItem"/>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.item-list {
    display: flex;
    flex-wrap: wrap;
    column-gap: 10px;
    row-gap: 10px;
}
.item-card-list{
}
</style>