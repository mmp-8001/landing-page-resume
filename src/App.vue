<template>
  <Ads/>
  <Navbar/>
</template>

<script setup lang="ts">
import Ads from './components/Ads.vue'
import Navbar from './components/Navbar.vue'

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
}

a {
  text-decoration: none;
  color: inherit;
}
</style>
