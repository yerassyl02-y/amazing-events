<template>
  <div class="partners">
    <swiper ref="swiper2" class="swiper" :options="swiperOptions">
      <swiper-slide v-for="(item, idx) in partners" :key="idx">
        <img :src="item.image" />
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  data() {
    return {
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
      partners: [
        {
          image: require("@/assets/images/partners/1fit.jpeg"),
        },
        {
          image: require("@/assets/images/partners/bcc.png"),
        },
        {
          image: require("@/assets/images/partners/pinup.png"),
        },
        {
          image: require("@/assets/images/partners/sportmaster.svg"),
        },
        {
          image: require("@/assets/images/partners/technodom.jpeg"),
        },
        {
          image: require("@/assets/images/partners/wildberries.jpeg"),
        },
        {
          image: require("@/assets/images/partners/yandex.png"),
        },
      ],
    };
  },
};
</script>
