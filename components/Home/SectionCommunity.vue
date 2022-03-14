<template>
  <div class="community">
    <div class="community__container custom_container">
      <h3 class="community__title">
        An evolving community for an evolving DeFi landscape
      </h3>
      <div class="community__list">
        <SharedCard :data="item" v-for="(item, index) in data" :key="index" />
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

.community {
  .community__container {
    padding-top: 60px;
    padding-bottom: 40px;
  }

  .community__title {
    text-align: center;
    margin-bottom: 40px;
    font-size: 24px;

    @include breakpoint(md) {
      margin: 0 auto 40px;
      font-size: 36px;
      max-width: 700px;
    }
  }

  .community__list {
    display: grid;
    grid-template-columns: 1fr;
    column-gap: 24px;
    row-gap: 24px;

    @include breakpoint(sm) {
      grid-template-columns: repeat(2, 1fr);
    }

    @include breakpoint(lg) {
      grid-template-columns: repeat(4, 1fr);
    }
  }
}
</style>
