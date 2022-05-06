<template>
  <div class="navbar container">
    <div class="row flex-nowrap justify-content-center">
      <div class="col-2 logo">BRAND LOGO</div>
      <div class="col-2 menu">
        <span class="icon-menu"></span>
        <span>دسته‌بندی</span>
        <span class="icon-arrow-down"></span>
      </div>
      <div class="col-4">
        <SearchBar/>
      </div>
      <div class="col phone">
        <div>
          <span class="phone-area-code">041</span>
          <span class="phone-number">35564126</span>
        </div>
        <span class="icon-Telephone">
          <span class="path1"></span>
          <span class="path2"></span>
        </span>
      </div>
      <div class="col-1 shop">
        <span class="shop-count">3</span>
        <span class="icon-shopping-cart">
          <span class="path1"></span>
          <span class="path2"></span>
          <span class="path3"></span>
          <span class="path4"></span>
        </span>
      </div>
      <div class="col justify-content-end user-account">
        <span class="icon-user"></span>
        <span class="user_name">پژمان فرجی</span>
        <span class="icon-arrow-down"></span>
      </div>
    </div>
  </div>
</template>

<script setup>
import {ref} from 'vue'
import SearchBar from './SearchBar.vue'
</script>

<style scoped lang="scss">

$text_main_color: #0D0D0D;

.navbar {
  color: $text_main_color;
  margin-top: 20px;
  font-size: 18px;

  .row > div {
    display: flex;
    align-items: center;
  }

  .logo {
    font-weight: 500;
    font-size: 20px;
    color: #707070;
  }

  .shop {
    position: relative;
    justify-content: center;

    .shop-count {
      display: flex;
      justify-content: center;
      align-items: center;
      position: absolute;
      font-size: 18px;
      font-weight: 600;
      border-radius: 50%;
      background-color: #EF1E1E;
      color: white;
      width: 32px;
      height: 32px;
      top: 59%;
      left: 59%;
    }

    .icon-shopping-cart {
      font-size: 27px;
      padding: 10px;
      border: 2px solid #EBEBEB;
      border-radius: 10px;
    }
  }

  .phone {
    justify-content: end;
    column-gap: 10px;
    font-weight: bold;

    .icon-Telephone {
      font-size: 23px;
    }

    .phone-area-code {
      color: #9B9B9B;
      margin: 0 4px;
    }
  }

  .menu {
    column-gap: 10px;

    .icon-menu {
      font-size: 23px;
    }
  }

  .user-account {
    column-gap: 15px;

    .icon-user {
      color: #0066FF;
      padding: 16px;
      font-size: 19px;
      background-color: #E5EFFF;
      border-radius: 50%;
    }

    .user_name {
      white-space: nowrap;
    }
  }

  .icon-arrow-down {
    font-size: 11px;
    color: #9B9B9B;
  }
}
</style>