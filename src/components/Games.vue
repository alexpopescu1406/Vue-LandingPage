<template>
   <div
    data-aos="flip-left"
    data-aos-delay="50"
    data-aos-duration="2000"
    data-aos-easing="ease-out-back"
    data-aos-mirror="false"
    data-aos-once="true"
    data-aos-offset="500">
    
  <p class="gamestext">{{ games }}</p>
  <swiper
    :spaceBetween="30"
    :effect="'fade'"
    :navigation="true"
    :pagination="{
      clickable: true,
    }"
    :modules="modules"
    class="mySwiper">
    <swiper-slide> <img :src="require('../../images/slide1.jpg')" alt="slide1" /> </swiper-slide>
    <swiper-slide> <img :src="require('../../images/slide2.jpg')" alt="slide2" /> </swiper-slide> 
    <swiper-slide> <img :src="require('../../images/slide3.jpg')" alt="slide3" /> </swiper-slide>
    <swiper-slide> <img :src="require('../../images/slide1.jpg')" alt="slide1" /> </swiper-slide>
  </swiper>
  </div>
</template>

<script>
import { Swiper, SwiperSlide } from "swiper/vue";

import "swiper/css";

import "swiper/css/effect-fade";
import "swiper/css/navigation";
import "swiper/css/pagination";

import "../../public/style.css";

import { EffectFade, Navigation, Pagination } from "swiper";

export default {
  components: {
    Swiper,
    SwiperSlide,
  },
  setup() {
    return {
      modules: [EffectFade, Navigation, Pagination],
      games: 'GAMES',
    }
  },
}
</script>

<style>
.gamestext{
    color:white;
    text-align: center;
    font-size: 30px;
    font-weight: bold;
}
</style>