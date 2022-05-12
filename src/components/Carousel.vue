<script>
// Import Background Images
import backgroundBattery from '../assets/img/battery.webp';
import backgroundHeadphone from '../assets/img/headphone.jpeg';
import backgroundPhone from '../assets/img/phone.png';

// Import Swiper Vue.js components
import {Swiper, SwiperSlide} from "swiper/vue";
import Card from "./Card.vue";

// Import Swiper styles
import "swiper/css";

import "swiper/css/free-mode"
import "swiper/css/thumbs"
import "swiper/css/effect-fade";
import "swiper/css/pagination";

// import required modules
import {EffectFade, FreeMode, Thumbs} from "swiper";
import {ref} from "vue";

export default {
  components: {
    Swiper,
    SwiperSlide,
    Card
  },
  setup() {
    const thumbsSwiper = ref(null);

    const setThumbsSwiper = (swiper) => {
      thumbsSwiper.value = swiper;
    }

    return {
      thumbsSwiper,
      setThumbsSwiper,
      backgroundPhone,
      backgroundHeadphone,
      backgroundBattery,
      modules: [EffectFade, FreeMode, Thumbs],
    };
  },
};
</script>

<template>
  <div class="container">
    <div class="row">
      <swiper
          @swiper="setThumbsSwiper"
          :breakpoints="{'1200':{direction:'vertical'}}"
          :slidesPerView="3"
          :modules="modules"
          class="side-button col-xl-3 col-12 order-xl-first order-last d-none d-lg-block"
      >
        <swiper-slide>
          <Card class="thumb d-flex flex-row align-items-center justify-content-center">
            <span class="icon icon-battery-charging"></span>
            <div class="info d-flex flex-column">
              <span class="title">باتری انواع دستگاه ها</span>
              <span class="detail">موبایل، تبلت، ساعت هوشمند</span>
            </div>
          </Card>
        </swiper-slide>
        <swiper-slide>
          <Card class="thumb d-flex flex-row align-items-center justify-content-center">
            <span class="icon icon-cpu-setting"><span class="path1"></span><span class="path2"></span><span
                class="path3"></span><span class="path4"></span><span class="path5"></span><span
                class="path6"></span><span class="path7"></span><span class="path8"></span><span
                class="path9"></span><span class="path10"></span><span class="path11"></span><span
                class="path12"></span></span>
            <div class="info d-flex flex-column">
              <span class="title">قطعات سخت افزاری</span>
              <span class="detail">صفحه نمایش، حافظه، دوربین</span>
            </div>
          </Card>
        </swiper-slide>
        <swiper-slide>
          <Card class="thumb d-flex flex-row align-items-center justify-content-center">
            <span class="icon icon-headphones"><span class="path1"></span><span class="path2"></span><span
                class="path3"></span><span class="path4"></span><span class="path5"></span><span
                class="path6"></span><span class="path7"></span><span class="path8"></span></span>
            <div class="info d-flex flex-column">
              <span class="title">انواع لوازم جانبی</span>
              <span class="detail">قاب، هندزفری، انواع کابل شارژ</span>
            </div>
          </Card>
        </swiper-slide>
      </swiper>
      <swiper
          :effect="'fade'"
          :thumbs="{ swiper: thumbsSwiper }"
          :modules="modules"
          :loop="true"
          class="main-slider col-12 col-xl-9 order-first order-xl-last"
      >
        <swiper-slide>
          <div class="slider" :style="{backgroundImage: `url(${backgroundBattery} )`}">
            <div class="content d-none d-lg-block">
              <div class="wrapper d-flex align-items-between flex-column">
                <div class="title">بررسی انواع آیفون در گروه فنی استارموبو</div>
                <div class="desc">لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان
                  گرافیک
                  است
                </div>
              </div>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="slider" :style="{backgroundImage: `url(${backgroundBattery} )`}">
            <div class="content d-none d-lg-block">
              <div class="wrapper d-flex align-items-between flex-column">
                <div class="title">بررسی انواع آیفون در گروه فنی استارموبو</div>
                <div class="desc">لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان
                  گرافیک
                  است
                </div>
              </div>
            </div>
          </div>
        </swiper-slide>
        <swiper-slide>
          <div class="slider" :style="{backgroundImage: `url(${backgroundBattery} )`}">
            <div class="content d-none d-lg-block">
              <div class="wrapper d-flex align-items-between flex-column">
                <div class="title">بررسی انواع آیفون در گروه فنی استارموبو</div>
                <div class="desc">لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ و با استفاده از طراحان
                  گرافیک
                  است
                </div>
              </div>
            </div>
          </div>
        </swiper-slide>
      </swiper>
    </div>
  </div>
</template>
<style lang="scss">
$vertical-space: 40px;

.main-slider {
  padding-top: $vertical-space;
  padding-bottom: $vertical-space;

  .swiper-slide {
    border-radius: 10px;
    position: relative;
    padding-top: 75%;
    overflow: hidden;

    &.swiper-slide-active .slider .content {
      opacity: 1;
      transform: translate(-50%, 0);
    }

    .slider {
      position: absolute;
      left: 0;
      top: 0;
      width: 100%;
      height: 100%;
      background-size: cover;
      background-repeat: no-repeat;
      background-position: center center;

      .content {
        transition: all 250ms ease-in-out;
        width: 100%;
        left: 50%;
        bottom: 0;
        position: absolute;
        transform: translate(-50%, 100px);
        padding: 2em;
        opacity: 0;

        .wrapper {
          padding: 20px;
          background-color: rgba(255, 255, 255, 0.7);
          border-radius: 10px;
          row-gap: 10px;

          .title {
            font-weight: 600;
          }

          .desc {
            color: #0D0D0D;
            font-size: 15px;
          }
        }
      }
    }
  }
}

.side-button {
  padding-top: $vertical-space;
  padding-bottom: $vertical-space;

  .thumb {
    column-gap: 20px;
    width: 100%;
    cursor: pointer;
    transition: all 250ms ease-in-out;
    padding: 20px 0;

    .title {
      font-weight: 600;
    }

    .detail {
      transition: all 250ms ease-in-out;
      font-size: 15px;
      color: #9B9B9B;
    }

    .icon {
      font-size: 30px;
      padding: 10px;
      border-radius: 10px;
      background-color: #E5EFFF;
    }
  }

  .swiper-slide.swiper-slide-thumb-active .thumb, .thumb:hover {
    background-color: #0066FF;
    color: white;

    .detail {
      color: #B4D1FF;
    }

    .icon {
      background-color: #4E92FF;
    }
  }

  .swiper-wrapper {
    display: flex;
    flex-direction: row;
    justify-content: space-between;

    .swiper-slide {
      display: flex;
      height: auto;
      width: 100%;
      padding: 0 5px;

      &:last-child {
        padding-left: 0;
      }

      &:first-child {
        padding-right: 0;
      }
    }
  }
}

// Large devices (desktops, 992px and up)
@media (min-width: 992px) {
  .main-slider {
    padding-bottom: 0;

    .swiper-slide {
      padding-top: 50%;
    }
  }
}

// X-Large devices (large desktops, 1200px and up)
@media (min-width: 1200px) {
  .main-slider {
    padding-bottom: $vertical-space;
  }
  .side-button {
    .swiper-wrapper {
      flex-direction: column;

      .swiper-slide {
        padding: 0 0 20px 0;

        &:last-child {
          padding: 0;
        }
      }
    }
  }
}
</style>