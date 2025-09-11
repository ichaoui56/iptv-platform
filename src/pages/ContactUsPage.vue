<template>
  <NavbarOne />
  <PageBanner
    pageTitle="CONTACT US"
    subTitle="Your direct line to seamless support and information – Reach out to our dedicated team at Nestor"
    :pageBannerImage="pageBannerImg"
  />
  <ContactInfo />
  <SendUsMessage />
  <PartnerLogo />
  <SubscribeContent />
  <MainFooter class="bg-black" />
  <CopyRight />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import NavbarOne from "@/components/Layouts/NavbarOne.vue";
import PageBanner from "@/components/Common/PageBanner.vue";
import ContactInfo from "@/components/ContactUs/ContactInfo.vue";
import SendUsMessage from "@/components/ContactUs/SendUsMessage.vue";
import PartnerLogo from "@/components/ContactUs/PartnerLogo.vue";
import SubscribeContent from "@/components/Common/SubscribeContent.vue";
import MainFooter from "@/components/Layouts/MainFooter.vue";
import CopyRight from "@/components/Layouts/CopyRight.vue";

export default defineComponent({
  name: "ContactUsPage",
  components: {
    NavbarOne,
    PageBanner,
    ContactInfo,
    SendUsMessage,
    PartnerLogo,
    SubscribeContent,
    MainFooter,
    CopyRight,
  },
  setup() {
    // eslint-disable-next-line @typescript-eslint/no-var-requires
    const pageBannerImg = require("@/assets/images/page-banner-7.jpg");

    return {
      pageBannerImg,
    };
  },
});
</script>
