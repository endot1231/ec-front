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
    <div class="icon-list">
        <AtomsIconsHeart @clickIcon="clickHeart" />
        <AtomsIconsBell @clickIcon="clickBell" />
        <AtomsIconsCart @clickIcon="clickCart" />
    </div>
</template>

<style lang="scss" scoped>
.icon-list {
    display: flex;
}
</style>