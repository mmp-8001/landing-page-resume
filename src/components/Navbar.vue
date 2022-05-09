<template>
  <div class="navbar container">
    <div class="row flex-lg-nowrap flex-wrap justify-content-center">
      <div class="col-lg-2 order-lg-0 order-1 col-6 justify-content-lg-start justify-content-center logo"><span>BRAND LOGO</span>
      </div>
      <div class="col-lg-2 justify-content-start justify-content-lg-center justify-content-xl-start col-3">
        <Menu/>
      </div>
      <div class="col-lg-4 col-10 order-lg-3 order-4">
        <SearchBar/>
      </div>
      <div class="col phone order-lg-4 d-lg-flex d-none">
        <div>
          <span class="phone-area-code">041</span>
          <span class="phone-number">35564126</span>
        </div>
        <span class="icon-Telephone">
          <span class="path1"></span>
          <span class="path2"></span>
        </span>
      </div>
      <div
          class="col-xxl-1 col-lg-auto col-2 align-items-center justify-content-end order-last order-lg-5 justify-content-lg-center">
        <Cart/>
      </div>
      <div class="divider d-xl-none col align-items-stretch order-5 d-none d-lg-flex"><span>&nbsp;</span></div>
      <div class="col-lg-auto justify-content-end order-lg-last order-3 col-3">
        <UserAccount/>
      </div>
    </div>
  </div>
</template>

<script setup>
import {ref} from 'vue'
import SearchBar from './SearchBar.vue'
import UserAccount from './UserAccount.vue'
import Cart from './Cart.vue'
import Menu from './Menu.vue'
</script>

<style scoped lang="scss">
$text_main_color: #0D0D0D;
$vertical-space: 40px;

.navbar {
  color: $text_main_color;
  margin-top: $vertical-space;
  font-size: 15px;

  & > .row {
    row-gap: 20px;
  }

  .divider span {
    background-color: rgba(0, 0, 0, 0.08);
  }

  .row > div {
    display: flex;
    align-items: center;
  }

  .logo {
    font-weight: 500;
    font-size: 25px;
    margin-top: 8px;
    white-space: nowrap;
    color: #707070;
  }

  .phone {
    justify-content: end;
    column-gap: 10px;
    font-weight: 500;

    .icon-Telephone {
      font-size: 21px;
    }

    .phone-area-code {
      color: #9B9B9B;
      margin: 0 4px;
    }
  }
}
</style>