<template>
  <div class="information">
    <div class="information__container custom_container">
      <div class="information__list">
        <div
          class="information__card"
          v-for="(item, index) in data"
          :key="index"
        >
          <div class="information__title">{{ item.title }}</div>
          <div class="information__description">{{ item.description }}</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import SharedCard from "@/components/Shared/Card";

export default {
  props: {
    data: Array
  },
  components: {
    SharedCard
  }
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";

.information {
  .information__container {
    padding-top: 20px;
    padding-bottom: 20px;
  }

  .information__list {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    column-gap: 24px;
    row-gap: 24px;

    @include breakpoint(lg) {
      grid-template-columns: repeat(4, 1fr);
    }
  }

  .information__card {
    width: 100%;
    padding: 32px 0;
    background: #202231;
    border-radius: 6px;
    text-align: center;
  }

  .information__title {
    font-size: 36px;
    font-weight: 600;
  }

  .information__description {
    color: #7f7f7f;
    font-size: 14px;
  }
}
</style>
