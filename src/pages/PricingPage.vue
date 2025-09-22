<template>
  <NavbarTwo />
  <PageBanner
    pageTitle="PRICING"
    subTitle="Explore our diverse range of High-Speed internet pricing plans tailored to fit Every need & budget"
    :pageBannerImage="pageBannerImg"
  />
  <PricingPlans />
  <TestOurService />
  <FAQ />
  <SubscribeContent />
  <MainFooter class="bg-black" />
  <CopyRight />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import NavbarTwo from "@/components/Layouts/NavbarTwo.vue";
import PageBanner from "@/components/Common/PageBanner.vue";
import PricingPlans from "@/components/Pricing/PricingPlans.vue";
import TestOurService from "@/components/Pricing/TestOurService.vue";
import FAQ from "@/components/Pricing/FAQ.vue";
import SubscribeContent from "@/components/Common/SubscribeContent.vue";
import MainFooter from "@/components/Layouts/MainFooter.vue";
import CopyRight from "@/components/Layouts/CopyRight.vue";

export default defineComponent({
  name: "PricingPage",
  components: {
    NavbarTwo,
    PageBanner,
    PricingPlans,
    TestOurService,
    FAQ,
    SubscribeContent,
    MainFooter,
    CopyRight,
  },
  setup() {
    // eslint-disable-next-line @typescript-eslint/no-var-requires
    const pageBannerImg = require("@/assets/images/page-banner-4.jpg");

    return {
      pageBannerImg,
    };
  },
});
</script>
