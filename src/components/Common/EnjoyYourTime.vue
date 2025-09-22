<template>
  <div class="movies-area pb-100">
    <div class="container mw-1356">
      <div
        class="section-title mw-690 m-auto text-center"
        data-aos="fade-up"
        data-aos-duration="1000"
        data-aos-delay="100"
      >
        <span class="top-title">ENJOY YOUR TIME</span>
        <h2 :class="className">
          Enjoy watching now Movies, Series, Shows, Anime and More
        </h2>
      </div>
    </div>

    <div class="container-fluid p-0">
      <Swiper
        :slidesPerView="1"
        :spaceBetween="24"
        :centeredSlides="false"
        :preventClicks="true"
        :loop="true"
        :autoplay="{
          delay: 8000,
          disableOnInteraction: false,
          pauseOnMouseEnter: false,
        }"
        :breakpoints="{
          0: {
            slidesPerView: 1,
          },
          576: {
            slidesPerView: 2,
          },
          768: {
            slidesPerView: 3,
          },
          992: {
            slidesPerView: 4,
          },
          1200: {
            slidesPerView: 5,
          },
          1440: {
            slidesPerView: 6,
          },
        }"
        :modules="modules"
        class="movies-slide"
      >
        <SwiperSlide v-for="slide in slides" :key="slide.id">
          <RouterLink to="/services-details">
            <img :src="slide.image" alt="movie" style="width: 100%; height:400px"/>
          </RouterLink>
        </SwiperSlide>
      </Swiper>
    </div>

    <div class="text-center mt-4 pt-1">
      <p class="text-silver">Everything you need to enjoy your time</p>
      <RouterLink to="/pricing-plan" class="btn">
        <span class="border-style">Get It Now</span>
      </RouterLink>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay } from "swiper/modules";

export default defineComponent({
  name: "EnjoyYourTime",
  components: {
    Swiper,
    SwiperSlide,
  },
  props: ["className"],
  data() {
    return {
      slides: [
        {
          id: 1,
          image: require("@/assets/images/movie-home/movie1.jpg"),
        },
        {
          id: 2,
          image: require("@/assets/images/tv-shows/tv-show1.jpeg"),
        },
        {
          id: 3,
          image: require("@/assets/images/anime/anime1.jpeg"),
        },
        {
          id: 4,
          image: require("@/assets/images/movie-home/movie4.jpg"),
        },
        {
          id: 5,
          image: require("@/assets/images/tv-shows/tv-show2.jpeg"),
        },
        {
          id: 6,
          image: require("@/assets/images/anime/anime2.jpeg"),
        },
        {
          id: 7,
          image: require("@/assets/images/movie-home/movie7.jpg"),
        },
        {
          id: 8,
          image: require("@/assets/images/tv-shows/tv-show3.jpeg"),
        },
        {
          id: 9,
          image: require("@/assets/images/anime/anime3.jpeg"),
        },
        {
          id: 10,
          image: require("@/assets/images/movie-home/movie10.jpg"),
        },
        {
          id: 11,
          image: require("@/assets/images/tv-shows/tv-show4.jpeg"),
        },
        {
          id: 12,
          image: require("@/assets/images/anime/anime4.jpeg"),
        },
        {
          id: 13,
          image: require("@/assets/images/movie-home/movie13.jpg"),
        },
        {
          id: 14,
          image: require("@/assets/images/tv-shows/tv-show5.jpeg"),
        },
        {
          id: 15,
          image: require("@/assets/images/anime/anime5.jpeg"),
        },
        {
          id: 16,
          image: require("@/assets/images/movie-home/movie16.jpg"),
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
