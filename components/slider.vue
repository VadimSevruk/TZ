<!-- You can custom the "mySwiper" name used to find the swiper instance in current component -->
<template>
  <!-- <div class="swiper" v-tooltip.top-center="msg"> -->
  <div class="swiper" v-bind:title="msg">
    <div v-swiper:mySwiper="swiperOption">
      <div class="swiper-wrapper">
        <div class="swiper-slide" v-for="banner in banners" :key="banner">
          <!-- <img :src="banner"> -->
          <span>{{ banner }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      banners: ["Ink Lingerie", "Ink Lingerie", "Ink Lingerie"],
      swiperOption: {
        slidesPerView: 2,
        centeredSlides: true,
        loop: true,
        spaceBetween: 317,
        breakpoints: {
          1024: {
            slidesPerView: 1.9,
            spaceBetween: 198
          },
          768: {
            slidesPerView: 1.6,
            spaceBetween: 118
          },
          414: {
            slidesPerView: 1.45,
            spaceBetween: 56
          },
          375: {
            slidesPerView: 1.4,
            spaceBetween: 46
          }
        }
      },
      msg: "DRAG ME"
    };
  },
};
</script>

<style lang="less">
.swiper {
      padding-top: 265px;
}

.swiper-slide {
  font-family: "Cond";
  font-size: 125.581px;
  line-height: 86%;
  text-transform: uppercase;
  -webkit-text-stroke: 0.837209px #580300;
  -webkit-text-fill-color: transparent;
  width: fit-content !important;
  text-align: center;
  letter-spacing: 8px;

  &-prev {
    transform: rotate(-1.5deg);
  }

  &-next {
    transform: rotate(1.5deg);
  }

  &-active {
    -webkit-text-fill-color: #580300;
    -webkit-text-stroke: 0;
  }
}

@media only screen and (max-width: 1024px) {
  .swiper {
    padding-top: 165px;
  }

  .swiper-slide {
    font-size: 96px;
  }
}

@media only screen and (max-width: 768px) {
  .swiper {
    padding-top: 330px;
  }
}

@media only screen and (max-width: 414px) {
  .swiper {
    padding-top: 270px;
  }

  .swiper-slide {
    font-size: 48px;
  }
}

@media only screen and (max-width: 375px) {
  .swiper {
    padding-top: 240px;
  }

  .swiper-slide {
    font-size: 44px;
  }
}
</style>