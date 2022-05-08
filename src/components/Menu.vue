<template>
  <DropDown class="menu align-items-center d-none d-lg-flex flex-nowrap">
    <template #dropdown>
      <span class="icon-menu"></span>
      <span class="d-none d-lg-inline">دسته‌بندی</span>
      <span class="icon-arrow-down d-none d-lg-inline"></span>
    </template>
    <template #content>
      <Card class="menu-content d-flex flex-row flex-nowrap">
        <div class="menu-item d-flex flex-column">
          <div class="d-flex item flex-nowrap align-items-center justify-content-between"><span>باتری</span><span
              class="icon-arrow-left"></span></div>
          <div class="d-flex item flex-nowrap align-items-center justify-content-between"><span>ساعت هوشمند</span><span
              class="icon-arrow-left"></span></div>
          <div class="d-flex item flex-nowrap align-items-center justify-content-between"><span>قطعات</span><span
              class="icon-arrow-left"></span></div>
          <div class="d-flex item flex-nowrap align-items-center justify-content-between"><span>لوازم جانبی</span><span
              class="icon-arrow-left"></span></div>
          <div class="d-flex item flex-nowrap align-items-center justify-content-between"><span>نقد و بررسی</span><span
              class="icon-arrow-left"></span></div>
          <div class="d-flex item flex-nowrap align-items-center justify-content-between"><span>آموزش</span><span
              class="icon-arrow-left"></span></div>
        </div>
        <div class="divider">&nbsp;</div>
        <div class="item-content row flex-nowrap">
          <div class="col d-flex flex-column">
            <span class="header">باتری موبایل</span>
            <div class="content d-flex flex-column">
              <span class="item">(SAMSUNG)  سامسونگ</span>
              <span class="item">(Lenovo) لنوو</span>
              <span class="item"> (Acer) ایسر</span>
              <span class="item">(SONY)  سونی</span>
              <span class="item"> (HTC) اچ تی سی</span>
              <span class="item"> (Alcatel) آلکاتل</span>
              <span class="item">سایر برندها</span>
            </div>
          </div>
          <div class="col d-flex flex-column">
            <span class="header">باتری تبلت</span>
            <div class="d-flex flex-column content">
              <span class="item">(SAMSUNG)  سامسونگ</span>
              <span class="item">(HUAWEI)  هواوی</span>
              <span class="item">(Apple)  اپل</span>
              <span class="item">(SONY)  سونی</span>
              <span class="item">(LG) ال  جی</span>
              <span class="item">(NOKIA)  نوکیا</span>
              <span class="item">سایر برندها</span>
            </div>
          </div>
          <div class="col d-flex flex-column">
            <span class="header">باتری ساعت هوشمند</span>
            <div class="content d-flex flex-column">
              <span class="item">(SAMSUNG)  سامسونگ</span>
              <span class="item">(HUAWEI)  هواوی</span>
              <span class="item">(Apple)  اپل</span>
              <span class="item">(SONY)  سونی</span>
              <span class="item">(LG) ال  جی</span>
              <span class="item">(NOKIA)  نوکیا</span>
              <span class="item">سایر برندها</span>
            </div>
          </div>
          <div class="col d-flex flex-column">
            <span class="header">باتری قلمی</span>
            <div class="content d-flex flex-column">
              <span class="item">(OSEL)  اوسل</span>
              <span class="item">(ONIX)  اونیکس</span>
              <span class="item">(DAEWOO)  دوو</span>
              <span class="item">(DBK)  دی بی کی</span>
              <span class="item">(SONY)  سونی</span>
              <span class="item">(HYUNDAI)  هیوندای</span>
              <span class="item">سایر برندها</span>
            </div>
          </div>
          <div class="col d-flex flex-column">
            <div class="header d-flex flex-nowrap align-items-center"><span>سایر باتری ها</span><span
                class="icon-arrow-left"></span></div>
            <div class="content d-flex flex-column">
              <img src="src/assets/img/battery.png" alt="">
            </div>
          </div>
        </div>
      </Card>
    </template>
  </DropDown>
  <MobileMenu>
    <div class="menu align-items-center d-lg-none d-flex flex-nowrap">
      <span class="icon-menu"></span>
    </div>
  </MobileMenu>
</template>

<script setup>
import DropDown from './DropDown.vue'
import Card from './Card.vue'
import MobileMenu from './MobileMenu.vue'

</script>

<style scoped lang="scss">
$primary-color: #0D0D0D;
$secondary-color: #9B9B9B;
$select-color: #0066FF;
$hover-color: #E5EFFF;
$border-space: 20px;

.menu {
  column-gap: 10px;
  height: 100%;
  position: relative;
  cursor: pointer;

  .menu-content {
    position: absolute;
    width: auto;
    height: auto;
    right: -185%;
    top: calc(100% + 20px);

    .menu-item {
      margin: $border-space;

      .item {
        color: $primary-color;
        font-weight: 600;
        padding: 10px 20px;
        border-radius: 10px;
        cursor: pointer;
        transition: all 250ms ease-in-out;

        &:hover {
          color: $select-color;
          background-color: $hover-color;
        }
      }
    }

    .item-content {
      margin: $border-space;
      column-gap: 10px;

      .header {
        padding: 10px 0;
        font-weight: 500;
      }

      .content {
        row-gap: 10px;
        font-size: 13px;
        color: $secondary-color;

        .item {
          transition: all 250ms ease-in-out;

          &:hover {
            color: $select-color;
          }
        }
      }
    }

    .divider {
      width: 2px;
      background-color: #EBEBEB;
    }

    .icon-arrow-left {
      font-size: 12px;
      color: $secondary-color;
      margin-right: 20px;
    }
  }

  .icon-menu {
    font-size: 30px;
  }

  .icon-arrow-down {
    font-size: 10px;
    color: $secondary-color;
  }
}

// X-Large devices (large desktops, 1200px and up)
@media (min-width: 1200px) {
  .menu {
    .icon-menu {
      font-size: 19px;
    }

    .menu-content {
      right: 0;
    }
  }
}
</style>