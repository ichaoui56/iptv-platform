<template>
  <Swiper
    :slidesPerView="1"
    :spaceBetween="10"
    :centeredSlides="false"
    :preventClicks="true"
    :loop="true"
    :autoplay="{
      delay: 0,
      disableOnInteraction: false,
      pauseOnMouseEnter: true,
    }"
    :speed="18000"
    :direction="horizontal"
    :zoom="true"
    :keyboard="{
      enabled: true,
      onlyInViewport: false,
    }"
    :breakpoints="{
      0: {
        slidesPerView: 1,
      },
      576: {
        slidesPerView: 2,
      },
      450: {
        slidesPerView: 1,
      },
      768: {
        slidesPerView: 2,
      },
      992: {
        slidesPerView: 2.5,
      },
      1440: {
        slidesPerView: 3,
      },
      1600: {
        slidesPerView: 4,
      },
    }"
    :modules="modules"
    class="banner-slide-3"
  >
    <SwiperSlide v-for="slide in slides" :key="slide.id">
      <img :src="slide.image" alt="slide" />
    </SwiperSlide>
  </Swiper>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay } from "swiper/modules";

export default defineComponent({
  name: "BannerSlideThree",
  components: {
    Swiper,
    SwiperSlide,
  },
  data() {
    return {
      slides: [
        {
          id: 1,
          image: require("@/assets/images/iptv-hero/banner1/slide1.jpg"),
        },
        {
          id: 2,
          image: require("@/assets/images/iptv-hero/banner1/slide1.jpg"),
        },
        {
          id: 3,
          image: require("@/assets/images/iptv-hero/banner1/slide2.jpg"),
        },
        {
          id: 4,
          image: require("@/assets/images/iptv-hero/banner1/slide3.jpg"),
        },
        {
          id: 5,
          image: require("@/assets/images/iptv-hero/banner1/slide4.jpg"),
        },
        {
          id: 6,
          image: require("@/assets/images/iptv-hero/banner1/slide5.jpg"),
        },
        {
          id: 7,
          image: require("@/assets/images/iptv-hero/banner1/slide6.jpg"),
        },
        {
          id: 8,
          image: require("@/assets/images/iptv-hero/banner1/slide7.jpg"),
        },
        {
          id: 9,
          image: require("@/assets/images/iptv-hero/banner1/slide8.jpg"),
        },
        {
          id: 10,
          image: require("@/assets/images/iptv-hero/banner1/slide8.jpg"),
        },
      ],
    };
  },
  setup() {
    return {
      modules: [Autoplay],
    };
  },
});
</script>
