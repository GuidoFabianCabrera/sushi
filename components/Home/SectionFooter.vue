<template>
  <footer class="footer">
    <div class="footer__container custom_container custom_container--lg">
      <div class="footer__section">
        <div class="footer__logo">
          <img class="footer__image" src="images/logo.png" />
          <span class="footer__name">Sushi</span>
        </div>
        <div class="footer__description">
          Sushi is the home of DeFi. Our community is building a comprehensive,
          decentralized trading platform for the future of finance. Join us!
        </div>
        <div class="footer__social_list">
          <svg
            class="footer__social"
            xmlns="http://www.w3.org/2000/svg"
            fill="currentColor"
            clip-rule="evenodd"
            style="width:24px;height:24px;color:#9ca3af"
          >
            <path
              d="M2.846 6.887c.03-.295-.083-.586-.303-.784l-2.24-2.7v-.403h6.958l5.378 11.795 4.728-11.795h6.633v.403l-1.916 1.837c-.165.126-.247.333-.213.538v13.498c-.034.204.048.411.213.537l1.871 1.837v.403h-9.412v-.403l1.939-1.882c.19-.19.19-.246.19-.537v-10.91l-5.389 13.688h-.728l-6.275-13.688v9.174c-.052.385.076.774.347 1.052l2.521 3.058v.404h-7.148v-.404l2.521-3.058c.27-.279.39-.67.325-1.052v-10.608z"
            ></path>
          </svg>
          <span class="footer__social">
            <v-icon color="#9ca3af">mdi-twitter</v-icon>
          </span>
          <span class="footer__social">
            <v-icon color="#9ca3af">mdi-github</v-icon>
          </span>
        </div>
      </div>
      <div class="footer__section">
        <div class="footer__list">
          <div class="footer__list_item--title">PRODUCTS</div>
          <div class="footer__list_item">Swap</div>
          <div class="footer__list_item">Limit Order</div>
          <div class="footer__list_item">BentoBox Dapps</div>
          <div class="footer__list_item">Kashi Lending</div>
          <div class="footer__list_item">Kashi Borrow</div>
          <div class="footer__list_item">API</div>
        </div>
      </div>
      <div class="footer__section">
        <div class="footer__list">
          <div class="footer__list_item--title">SUPPORT</div>
          <div class="footer__list_item">Tutorials</div>
          <div class="footer__list_item">Documentation</div>
          <div class="footer__list_item">Discord</div>
          <div class="footer__list_item">Forum</div>
        </div>
      </div>
      <div class="footer__section">
        <div class="footer__list">
          <div class="footer__list_item--title">PROTOCOL</div>
          <div class="footer__list_item">Vote</div>
          <div class="footer__list_item">Create a Pair</div>
          <div class="footer__list_item">Register for Onsen</div>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";

.footer {
  padding-top: 70px;
  padding-bottom: 70px;
  background: #161522;

  .footer__container {
    display: flex;
    justify-content: space-between;
    row-gap: 40px;
    column-gap: 25px;
    flex-wrap: wrap;
  }

  .footer__section {
    max-width: 308px;
  }

  .footer__logo {
    display: flex;
    align-items: center;
  }

  .footer__image {
    width: 40px;
  }

  .footer__name {
    margin-left: 7px;
    font-size: 20px;
    font-weight: 700;
    color: white;
  }

  .footer__description {
    margin-top: 15px;
    color: #9ca3af;
    font-size: 14px;
  }

  .footer__social_list {
    margin-top: 15px;
    display: flex;
    align-content: center;
    column-gap: 20px;
  }

  .footer__list {
    display: flex;
    flex-direction: column;
    row-gap: 16px;
  }

  .footer__list_item {
    font-size: 16px;
    color: #9ca3af;
  }

  .footer__list_item--title {
    @extend .footer__list_item;
    font-size: 14px;
    font-weight: 600;
    color: white;
  }
}
</style>
