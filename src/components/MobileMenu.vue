<template>
  <div @click="show=true">
    <slot></slot>
  </div>
  <div v-show="show" class="overlay d-flex d-lg-none" @click="show=false"></div>
  <Transition>
    <div v-show="show" class="d-block d-lg-none" id="mobile-menu">
      <div class="profile-view d-flex flex-row align-items-center">
        <div class="photo d-flex justify-content-center align-items-center"><span class="icon-user"></span></div>
        <div class="details d-flex flex-column">
          <span class="name">پژمان فرجی</span>
          <span class="last-seen">آخرین ورود: 2 آبان 1400</span>
        </div>
      </div>
      <div class="divider"></div>
      <div class="d-flex flex-nowrap prof-ord justify-content-between">
        <a class="user-profile d-flex justify-content-between col-5">
          <span class="icon-user"></span>
          <span>پروفایل کاربری</span>
        </a>
        <span class="divider"></span>
        <a class="user-order d-flex justify-content-between col-5">
          <span class="icon-shopping-cart-ord"></span>
          <span>سفارشات من</span>
        </a>
      </div>
      <div class="divider"></div>
      <div class="saved-posts d-flex align-items-center">
        <span class="icon-battery-charging"></span>
        <span class="flex-grow-1">پست های ذخیره شده</span>
        <span class="posts-count">4</span>
      </div>
      <div class="divider"></div>
      <div class="menu-content">
        <Collapsible>
          <template #header>
            <span class="icon-search"></span>
            <span class="flex-grow-1">باتری</span>
          </template>
          <template #content>
            <Collapsible>
              <template #header>
                <span class="flex-grow-1">باتری موبایل</span>
              </template>
              <template #content>
                <a href="#">سامسونگ (SAMSUNG)</a>
                <a href="#">هواوی (HUAWEI)</a>
                <a href="#">هواوی (HUAWEI)</a>
                <a href="#">هواوی (HUAWEI)</a>
              </template>
            </Collapsible>
          </template>
        </Collapsible>

      </div>
    </div>
  </Transition>
</template>

<script setup>
import {ref} from 'vue'
import Collapsible from './Collapsible.vue'

const show = ref(true);
</script>
<style scoped lang="scss">
$background-color: #1f2631;
$primary-color: white;
$secondary-color: #9b9b9b;
$divider-color: rgb(49, 61, 80);
$border-space: 25px;
$content-padding: 15px;
$icon-spacing: 10px;

#mobile-menu {
  position: fixed;
  height: 100%;
  overflow-y: auto;
  top: 0;
  right: 0;
  background-color: $background-color;
  color: $primary-color;
  padding: $border-space 0;
  z-index: 15;

  .posts-count {
    display: flex;
    justify-content: center;
    align-items: center;
    font-size: 15px;
    font-weight: 600;
    border-radius: 50%;
    background-color: #EF1E1E;
    color: white;
    margin: -10px 0;
    width: 30px;
    height: 30px;
  }

  .profile-view {
    padding-bottom: $border-space;
    column-gap: 15px;

    .photo {
      padding: 20px;
      background-color: $divider-color;
      border-radius: 50%;

      .icon-user {
        font-size: 30px;
        color: white;
      }
    }

    .details {
      .last-seen {
        color: $secondary-color;
        font-size: 15px;
      }
    }
  }

  .saved-posts {
    padding: $content-padding 0;
    column-gap: $icon-spacing;
  }

  & > div:not(.divider) {
    margin: 0 $border-space;
  }

  .prof-ord {
    column-gap: 20px;
    padding: $content-padding 0;

    .user-profile, .user-order {
      column-gap: $icon-spacing;
    }
  }

  .divider {
    padding-top: 1px;
    padding-right: 1px;
    background-color: $divider-color;
  }

  [class^='icon'] {
    color: $secondary-color;
    font-size: 20px;
  }
}

.overlay {
  position: fixed;
  background-color: rgba(13, 13, 13, 0.66);
  width: 100%;
  height: 100%;
  top: 0;
  right: 0;
  z-index: 10;
}

.v-enter-active,
.v-leave-active {
  transition: all 0.3s ease-in-out;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
  transform: translateX(100%);
}
</style>