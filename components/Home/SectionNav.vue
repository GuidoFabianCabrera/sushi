<template>
  <div class="nav">
    <div class="nav__container custom_container">
      <img class="nav__logo" src="images/logo.png" />
      <div class="nav__text">Sushi</div>
      <v-spacer></v-spacer>
      <div class="nav__button_container">
        <v-btn class="nav__button" color="#0d0e21" dark rounded
          >Enter App</v-btn
        >
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";

.nav {
  .nav__container {
    padding-top: 24px;
    display: flex;
    align-items: center;
  }

  .nav__logo {
    width: 40px;
  }

  .nav__text {
    margin-left: 7px;
    font-size: 20px;
    font-weight: 700;
    color: white;
  }

  .nav__button_container {
    background-image: radial-gradient(circle at top left, #016eda, #d900c0);
    padding: 4px;
    border-radius: 28px;
  }

  .nav__button {
    width: 115px;
    height: 36px;
    text-transform: none;
    letter-spacing: 0px;
  }
}
</style>
