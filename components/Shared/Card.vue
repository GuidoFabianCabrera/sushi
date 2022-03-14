<template>
  <div class="card" v-bind:class="{ 'card--image': data.image }">
    <div v-show="data.logo" class="card__logo_container">
      <img class="card__logo" :src="data.logo" />
    </div>
    <img v-show="data.image" class="card__image" :src="data.image" />
    <div
      class="card__title"
      v-bind:class="{ 'card__title--wide': data.hasFontWide }"
    >
      {{ data.title }}
    </div>
    <div
      class="card__description"
      v-bind:class="{ 'card__description--wide': data.hasFontWide }"
    >
      {{ data.description }}
    </div>
    <v-btn v-show="data.button" class="card__button" dark>{{
      data.button
    }}</v-btn>
  </div>
</template>

<script>
export default {
  props: {
    data: Object
  }
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";

.card {
  width: 100%;
  padding: 32px;
  background: #202231;
  border-radius: 6px;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  margin: 0 auto;
  max-width: 300px;

  @include breakpoint(md) {
    margin-top: 70px;
  }

  .card__logo_container {
    width: 123px;
    height: 123px;
    display: flex;
    justify-content: center;
    align-items: center;
    border-radius: 100%;
    background-image: linear-gradient(
      224.43deg,
      rgb(13, 4, 21) -16.69%,
      rgb(27, 33, 82) 86.36%
    );

    @include breakpoint(md) {
      margin: -50% auto 0;
    }
  }

  .card__logo {
    width: 80px;
    padding: 8px;
  }

  .card__image {
    width: 111px;
  }

  .card__title {
    font-size: 18px;
    font-weight: 600;
  }

  .card__title--wide {
    @extend .card__title;
    font-size: 36px;
  }

  .card__description {
    color: #7f7f7f;
    font-size: 14px;
  }

  .card__description--wide {
    @extend .card__description;
    font-size: 16px;
  }

  .card__button {
    width: 100%;
    height: 42px;
    margin-top: 12px;
    text-transform: capitalize;
    font-weight: 600;
    letter-spacing: 0;
    background: linear-gradient(to right, #016eda, #d900c0);
  }
}

.card--image {
  margin-top: 20px;
}
</style>
