<template>
  <div class="slider">
    <swiper
      :slides-per-view="3"
      :space-between="50"
      navigation
      :pagination="{ clickable: true }"
      :scrollbar="{ draggable: true }"
    >
      <swiper-slide>Slide 1</swiper-slide>
      <swiper-slide>Slide 2</swiper-slide>
      <swiper-slide>Slide 3</swiper-slide>

    </swiper>
  </div>
</template>

<script>
// import SwiperCore, { Navigation, Pagination } from 'swiper';
import { Swiper, SwiperSlide } from 'swiper/vue'

import 'swiper/swiper-bundle.min.css'

// SwiperCore.use([Navigation, Pagination]);

export default {
  name: "slider",
  components: { Swiper, SwiperSlide },
  data() {
    return {
      slides: [
        {
          image: require("../assets/images/slider/1.jpg")
        },
        {
          image: require("../assets/images/slider/2.jpg")
        },
        {
          image: require("../assets/images/slider/3.jpg")
        },
        {
          image: require("../assets/images/slider/4.jpg")
        },
        {
          image: require("../assets/images/slider/5.jpg")
        },
      ],
      swiperOptions: {
        slidesPerView: 3,
        spaceBetween: 30,
        slidesPerGroup: 3,
        loop: true,
        loopFillGroupWithBlank: true,
        pagination: {
          el: '.swiper-pagination',
          clickable: true,
        },
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev',
        },
      }
    }
  }
}
</script>

<style scoped>

  .swiper-slide {
    text-align: center;
    font-size: 18px;
    background: #fff;

    /* Center slide text vertically */
    display: -webkit-box;
    display: -ms-flexbox;
    display: -webkit-flex;
    display: flex;
    -webkit-box-pack: center;
    -ms-flex-pack: center;
    -webkit-justify-content: center;
    justify-content: center;
    -webkit-box-align: center;
    -ms-flex-align: center;
    -webkit-align-items: center;
  }

  .slider {
    @apply .mt-20
  }
  .swiper-slide {
    @apply .h-64
  }
</style>