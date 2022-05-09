<template>
  <div class="container">
    <div class="row">
      <div class="products">
        <swiper
            :slidesPerView="1"
            :spaceBetween="20"
            :breakpoints="{'768':{slidesPerView: 2},'992':{slidesPerView: 3},'1400':{slidesPerView: 4}}"
            :freeMode="true"
            :modules="modules"
            class="slider d-flex flex-column">
          <swiper-slide>
            <Product/>
          </swiper-slide>
          <swiper-slide>
            <Product/>
          </swiper-slide>
          <swiper-slide>
            <Product/>
          </swiper-slide>
          <swiper-slide>
            <Product/>
          </swiper-slide>
          <swiper-slide>
            <Product/>
          </swiper-slide>
          <swiper-slide>
            <Product/>
          </swiper-slide>

        </swiper>
      </div>
    </div>
  </div>
</template>

<script setup>
import Product from './Product.vue'
import {Swiper, SwiperSlide} from "swiper/vue";
import "swiper/css";
import "swiper/css/free-mode";
import {ref} from "vue";
import {FreeMode} from "swiper";

const modules = ref([FreeMode])
</script>

<style scoped lang="scss">
.products {
  .slider {
    background-color: #E5EFFF;
    border-radius: 10px;
    padding: 20px;
  }
}
</style>