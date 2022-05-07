<template>
  <div class="navbar container">
    <div class="row flex-nowrap justify-content-center">
      <div class="col-2 logo"><span>BRAND LOGO</span></div>
      <div class="col-2">
        <Menu/>
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
      <div class="col-1 align-items-center justify-content-center">
        <Cart/>
      </div>
      <div class="col">
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

// Colors
$text_main_color: #0D0D0D;

.navbar {
  color: $text_main_color;
  margin-top: 20px;
  font-size: 15px;

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