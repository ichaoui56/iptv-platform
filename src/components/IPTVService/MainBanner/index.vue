<template>
  <div class="banner-slide-area">
    <BannerSlideOne />

    <BannerSlideTwo />

    <BannerSlideThree />

    <div class="banner-content-wrap">
      <div class="container">
        <div
          class="banner-content"
          data-aos="fade-up"
          data-aos-duration="1000"
          data-aos-delay="100"
        >
          <span class="top-title">FAST IPTV CONNECTION</span>
          <h1>Enjoy Top Quality Streaming With Nestor IPTV</h1>
          <p>
            Includes all your favorite channels with local news, live sports,
            weather,
          </p>
          <form class="banner-form position-relative">
            <input
              type="text"
              class="form-control"
              placeholder="Search your content here"
            />
            <button
              type="submit"
              class="btn position-absolute top-50 end-0 translate-middle-y"
            >
              <span class="border-style">
                <span class="d-none d-sm-block">Search Now</span>
                <i class="ti ti-send d-sm-none"></i>
              </span>
            </button>
          </form>
          <ul
            class="ps-0 mb-0 list-unstyled d-flex align-items-center flex-wrap several-list gap-2 gap-lg-3 justify-content-center"
          >
            <li class="d-flex align-items-center">
              <i class="ti ti-circle-check"></i>
              <span>Connect several devices at once</span>
            </li>
            <li class="d-flex align-items-center">
              <i class="ti ti-circle-check"></i>
              <span>25,000 worldwide channels 4K</span>
            </li>
            <li class="d-flex align-items-center">
              <i class="ti ti-circle-check"></i>
              <span>500K new and old movies</span>
            </li>
          </ul>
        </div>

        <ul
          class="partner-logo ps-0 mb-0 list-unstyled d-none d-md-flex justify-content-lg-between flex-wrap gap-3 align-items-center justify-content-center"
          data-aos="fade-up"
          data-aos-duration="1000"
          data-aos-delay="200"
        >
          <li>
            <img src="@/assets/images/partner-7.png" alt="partner" />
          </li>
          <li>
            <img src="@/assets/images/partner-8.png" alt="partner" />
          </li>
          <li>
            <img src="@/assets/images/partner-9.png" alt="partner" />
          </li>
          <li>
            <img src="@/assets/images/partner-10.png" alt="partner" />
          </li>
          <li>
            <img src="@/assets/images/partner-11.png" alt="partner" />
          </li>
        </ul>

        <PartnerSlide />
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import BannerSlideOne from "./BannerSlideOne.vue";
import BannerSlideTwo from "./BannerSlideTwo.vue";
import BannerSlideThree from "./BannerSlideThree.vue";
import PartnerSlide from "./PartnerSlide.vue";

export default defineComponent({
  name: "MainBanner",
  components: {
    BannerSlideOne,
    BannerSlideTwo,
    BannerSlideThree,
    PartnerSlide,
  },
});
</script>
