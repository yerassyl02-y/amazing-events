<template>
  <div class="events">
    <div class="events__wrapper">
      <h2>Do not skip our events in Almaty</h2>
      <swiper ref="swiper" :options="swiperOptions" class="swiper">
        <swiper-slide
          v-for="(item, idx) in events"
          :key="idx"
          class="swiper-slide"
        >
          <div
            :style="{
              backgroundImage: `url(${item.image})`,
            }"
          >
            <h4>{{ item.title }}</h4>
          </div>
        </swiper-slide>
      </swiper>
      <button class="btn">
        <nuxt-link to="/events"> Watch more </nuxt-link>
      </button>
    </div>
  </div>
</template>

<script>
import Swiper, { Navigation, Pagination, Autoplay } from "swiper";
Swiper.use([, Navigation, Pagination, Autoplay]);
export default {
  data() {
    return {
      events: [
        {
          title: "Event 1",
          image: require("@/assets/images/events/image1.jpeg"),
        },
        {
          title: "Event 2",
          image: require("@/assets/images/events/image2.jpeg"),
        },
        {
          title: "Event 3",
          image: require("@/assets/images/events/image3.jpeg"),
        },
        {
          title: "Event 4",
          image: require("@/assets/images/events/image4.jpeg"),
        },
        {
          title: "Event 5",
          image: require("@/assets/images/events/image5.jpeg"),
        },
        {
          title: "Event 6",
          image: require("@/assets/images/events/image6.jpeg"),
        },
        {
          title: "Event 7",
          image: require("@/assets/images/events/image7.jpeg"),
        },
        {
          title: "Event 8",
          image: require("@/assets/images/events/image8.jpeg"),
        },
      ],
      swiperOptions: {
        slidesPerView: 1,
        spaceBetween: 20,
        speed: 500,
        transition: 5000,
        direction: "horizontal",
        pagination: {
          el: ".pagination1",
          clickable: true,
        },
        autoplay: {
          delay: 3000,
        },
        breakpoints: {
          1264: {
            slidesPerView: 4,
          },
          960: {
            slidesPerView: 3,
          },
          600: {
            slidesPerView: 2,
          },
        },
      },
    };
  },
};
</script>

<style>
</style>