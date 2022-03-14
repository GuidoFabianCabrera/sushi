<template>
  <div class="hero">
    <div class="hero__container custom_container">
      <img class="hero__image" src="images/thicker-neon.webp" />
      <h1 class="hero__title">Be a DeFi Chef with Sushi.</h1>
      <p class="hero__description">
        Swap, earn, stack yields, lend, borrow, leverage all on one
        decentralized, community driven platform. Welcome home to DeFi.
      </p>
      <v-btn class="hero__button--colors" dark>Enter App</v-btn>
      <v-btn class="hero__button" color="#2E3348" dark>Learn More</v-btn>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";

.hero {
  .hero__container {
    max-width: 698px;
    padding-top: 30px;
    padding-bottom: 30px;
    text-align: center;
  }

  .hero__image {
    width: 208px;
    margin-bottom: 15px;
  }

  .hero__title {
    font-size: 36px;
    font-weight: 600;
    line-height: 40px;
    margin-bottom: 32px;
  }

  .hero__description {
    margin-bottom: 40px;
    font-size: 18px;

    @include breakpoint(sm) {
    }
  }

  .hero__button {
    width: 100%;
    height: 48px;
    margin-bottom: 12px;
    text-transform: capitalize;
    font-weight: 600;
    @include breakpoint(sm) {
      width: 150px;
    }
  }

  .hero__button--colors {
    @extend .hero__button;
    background: linear-gradient(to right, #016eda, #d900c0);

    @include breakpoint(sm) {
      margin-right: 24px;
    }
  }
}
</style>
