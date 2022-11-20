<script setup lang="ts">
const emit = defineEmits<{
  (event: "clickItem", item_id: number): void;
}>();

const clickItem = (item_id: number) => {
  emit("clickItem", item_id);
};
</script>

<template>
  <nuxt-link to="/item/1" class="item-card">
    <div class="item-image">
      <div class="item-image-wrap">
        <img src="/img/sample.png" />
      </div>
    </div>
    <div class="item-text">
      <p class="item-title">イラスト</p>
      <div class="item-review">
        <UiStarReview />
        <object>
          <nuxt-link to="/item/1" class="item-review-link">4.0</nuxt-link>
        </object>
      </div>
      <p class="item-price">\ 4,000</p>
    </div>
  </nuxt-link>
</template>

<style lang="scss" scoped>
.item {
  &-card {
    display: block;
    padding: 5px;
    border-radius: 5px;
    text-decoration: none;
    border: #e5e5e5 1px solid;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.08);
  }
  &-image {
    padding-top: 28px;

    &-wrap {
      position: relative;
      padding-top: 100%;
    }
    img {
      position: absolute;
      margin: auto;
      top: 0;
      bottom: 0;
      left: 0;
      right: 0;
      max-width: 100%;
      max-height: 100%;
    }
  }

  &-text {
    padding-top: 5px;
    padding-bottom: 20px;
  }

  &-title {
    font-size: 16px;
    line-height: 24px;
    display: -webkit-box;
    -webkit-box-orient: vertical;
    -webkit-line-clamp: 2;
    overflow: hidden;
  }

  &-review {
    padding-top: 5px;
    display: flex;
    align-items: center;

    &-link {
      color: #007185;
      font-size: 14px;
      margin-left: 5px;

      &:hover {
        text-decoration: underline;
      }
    }
  }

  &-price {
    padding-top: 5px;
    display: flex;
    align-items: center;
    color: red;
    font-size: 14px;
  }

  @media screen and (max-width: 768px) {
    &-card {
      display: flex;
      align-items: center;
    }

    &-image {
      &-wrap {
        padding-top: 0;
      }
      img {
        max-height: 170px;
        max-width: 120px;
        position: static;
      }
    }
    &-text {
      padding-top: 0px;
      padding-bottom: 0px;
      padding-left: 10px;
    }
  }
}
</style>  