<template>
  <div class="app">
    <div class="main">
      <div class="main__background_container"></div>
      <div class="main__content">
        <HomeSectionNav />
        <HomeSectionHero />
        <HomeSectionInformation :data="information" />
      </div>
    </div>
    <HomeSectionInnovations :data="innovations" />
    <HomeSectionCommunity :data="community" />
    <HomeSectionPartners :data="partners" />
    <HomeSectionFooter :data="partners" />
  </div>
</template>

<script>
import HomeSectionNav from "@/components/Home/SectionNav";
import HomeSectionHero from "@/components/Home/SectionHero";
import HomeSectionInformation from "@/components/Home/SectionInformation";
import HomeSectionInnovations from "@/components/Home/SectionInnovations";
import HomeSectionCommunity from "@/components/Home/SectionCommunity";
import HomeSectionPartners from "@/components/Home/SectionPartners";
import HomeSectionFooter from "@/components/Home/SectionFooter";

export default {
  components: {
    HomeSectionNav,
    HomeSectionHero,
    HomeSectionInformation,
    HomeSectionInnovations,
    HomeSectionCommunity,
    HomeSectionPartners,
    HomeSectionFooter
  },
  data() {
    return {
      information: [
        { title: "$3.6", description: "$SUSHI Price" },
        { title: "$2B", description: "Total Liquidity" },
        { title: "$172.3B", description: "Total Volume" },
        { title: "2.6K", description: "Total Pairs" }
      ],
      innovations: [
        {
          title: "Multi-chain AMM",
          description:
            "The most competitive rates for DeFi bluechips anywhere. Switch to other chains in one click.",
          logo: "images/chopsticks.png",
          button: "Enter Exchange"
        },
        {
          title: "Kashi Lending & Leverage",
          description:
            "Isolated lending markets, elastic interest rates. Leverage long short or create your own market.",
          logo: "images/kashi-color-flat.png",
          button: "Enter Kashi"
        },
        {
          title: "xSUSHI staking",
          description:
            "Earn governance rights and 0.05% of all swaps from all chains in one simple place.",
          logo: "images/xsushi.png",
          button: "Enter SushiBar"
        },
        {
          title: "Onsen Program",
          description:
            "Accelerate your project with onsen. Find the best yields anywhere in DeFi hands down.",
          logo: "images/onsen-icon.png",
          button: "Browse Yields"
        }
      ],
      community: [
        {
          title: "20+",
          description: "Wallets Supported",
          image: "images/wallet.webp",
          hasFontWide: true
        },
        {
          title: "14",
          description: "Chains Supported",
          image: "images/intersection.webp",
          hasFontWide: true
        },
        {
          title: "25k+",
          description: "Discord Members",
          image: "images/group.webp",
          hasFontWide: true
        },
        {
          title: "150k+",
          description: "Sushi Holders",
          image: "images/sushi-outline.webp",
          hasFontWide: true
        }
      ],
      partners: [
        { title: "Yearn Finance", image: "images/yearn-neon.png" },
        { title: "CREAM Finance", image: "images/cream-neon.png" },
        { title: "Aave", image: "images/aave-neon.png" },
        { title: "Pickle Finance", image: "images/pickle-neon.png" },
        { title: "Akropolis", image: "images/akro-neon.png" },
        { title: "Keep3r Network", image: "images/keep3r-neon.png" }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/utils";

.app {
  // color: white;
  background: #0d0415;
}

.main {
  position: relative;

  .main__background_container {
    width: 100vw;
    height: 100%;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 0;
    background-image: url("https://guidofabiancabrera.github.io/sushi/images/background.jpg");
    background-size: cover;
    background-position: center;
  }

  .main__content {
    position: relative;
    z-index: 2;
  }
}
</style>
