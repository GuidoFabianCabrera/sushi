<template>
  <div class="partners">
    <div class="partners__container custom_container">
      <h3 class="partners__title">
        Meet the partners helping us cook up the tastiest dishes in DeFi.
      </h3>
      <div class="partners__list">
        <div class="partners__item" v-for="(item, index) in data" :key="index">
          <img :src="item.image" class="partners__image" />
          <div class="partners__title_item">{{ item.title }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SharedCard from "@/components/Shared/Card";

export default {
  props: { data: Array },
  components: { SharedCard }
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";

.partners {
  .partners__container {
    padding-top: 60px;
    padding-bottom: 60px;
  }

  .partners__title {
    text-align: center;
    margin-bottom: 40px;
    font-size: 24px;

    @include breakpoint(md) {
      margin: 0 auto 40px;
      font-size: 36px;
      max-width: 700px;
    }
  }

  .partners__list {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    column-gap: 24px;
    row-gap: 24px;

    @include breakpoint(sm) {
      grid-template-columns: repeat(3, 1fr);
    }

    @include breakpoint(lg) {
      grid-template-columns: repeat(6, 1fr);
    }
  }

  .partners__item {
    text-align: center;
  }

  .partners__image {
    width: 110px;
  }

  .partners__title_item {
    font-size: 16px;
    color: #6b7280;
  }
}
</style>
