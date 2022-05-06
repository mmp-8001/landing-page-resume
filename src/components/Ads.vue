<template>
  <Transition>
    <div v-if="show" class="ads">
      <img src="src/assets/img/ads.png" class="img" width="960" height="350" alt="">
      <div class="container content">
        <div class="content align-items-center d-flex">
          <div class="icon-close close" @click="show=!show"></div>
          <div class="text flex-grow-1 d-none d-md-block">جشنواره تابستانه دیجی‌کالا</div>
          <div class="text flex-grow-1 d-md-none ">جشنواره تابستانه استارموبو با جوایز و تخفیف ویژه</div>
        </div>
      </div>
    </div>

  </Transition>

</template>

<script setup>
import {ref} from 'vue'

// Toggle show
const show = ref(true)

</script>

<style scoped lang="scss">
div.ads {
  font-size: 18px;
  height: 60px;
  color: white;
  overflow: hidden;
  position: relative;

  .img {
    top: -205%;
    left: 0;
    position: absolute;
    width: 100%;
    height: auto;
  }

  .content {
    height: 100%;

    .close {
      cursor: pointer;
      z-index: 20;
    }

    .text {
      z-index: 10;
      position: absolute;
      width: 100%;
      left: 50%;
      top: 50%;
      text-align: center;
      transform: translate(-50%, -50%);
    }
  }
}

.v-enter-active,
.v-leave-active {
  transition: opacity 0.5s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}

// Medium devices (tablets, less than 992px)
@media (max-width: 991.98px) {
  div.ads {
    height: 50px;
    font-size: 14px;

    .img {
      top: -18%;
    }
  }
}


</style>