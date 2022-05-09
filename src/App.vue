<template>
  <Ads/>
  <Navbar/>
  <Carousel/>
  <ProductsSlider/>
</template>

<script setup lang="ts">
import Ads from './components/Ads.vue'
import Navbar from './components/Navbar.vue'
import Carousel from './components/Carousel.vue'
import ProductsSlider from './components/ProductsSlider.vue'

</script>

<style lang="scss">
@import "./styles/bootstrap-grid.rtl.min.css";
@import "./styles/fonts";
@import "./styles/icons.css";

@include font-yekan;


// Main config
body, html {
  direction: rtl !important;
  text-align: right !important;
  font-family: Yekan, Tahoma, sans-serif;
  font-weight: normal;
  margin: 0 !important;
  padding: 0 !important;
  background-color: #FFFFFF;
  scroll-behavior: smooth;
}

* {
  box-sizing: border-box;
  white-space: nowrap;
}

a {
  text-decoration: none;
  color: inherit;
  cursor: pointer;
}

/* width */
::-webkit-scrollbar {
  direction: rtl;
  width: 4px;
  transition: all 250ms ease-in-out;
}

/* Handle */
::-webkit-scrollbar-thumb {
  background: #9B9B9B;
  border-radius: 10px;
}

/* Handle on hover */
::-webkit-scrollbar-thumb:hover {
  background: #444444;
}
</style>
