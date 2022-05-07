<template>
  <DropDown class="d-flex align-items-center justify-content-end user-account">
    <template #dropdown>
      <span class="icon-user"></span>
      <span class="user_name">پژمان فرجی</span>
      <span class="icon-arrow-down"></span>
    </template>
    <template #content>
      <Card class="prof-card d-flex flex-column">
        <div class="prof-item"><span>پروفایل</span><span class="icon-arrow-down angle-left"></span></div>
        <div class="prof-item"><span>تاریخچه سفارشات</span><span class="icon-arrow-down angle-left"></span></div>
        <div class="prof-item danger"><span>خروج از حساب</span><span class="icon-arrow-down angle-left"></span></div>
      </Card>
    </template>
  </DropDown>
</template>

<script setup>
import Card from './Card.vue'
import DropDown from './DropDown.vue'

</script>

<style scoped lang="scss">
.user-account {
  column-gap: 15px;
  position: relative;
  cursor: pointer;

  .prof-card {
    row-gap: 10px;
    display: flex;
    width: calc(100% + 20px);
    height: auto;
    right: 0;
    padding: 10px;
    position: absolute;
    top: calc(100% + 20px);

    .prof-item {
      transition: all 0.3s ease-in-out;
      padding: 10px;
      border-radius: 10px;
      display: flex;
      align-items: center;
      justify-content: space-between;

      &.danger {
        background-color: #FEE8E8;
        color: #EF1E1E;

        .icon-arrow-down {
          color: #EF1E1E;
        }

        &:hover {
          background-color: #EF1E1E;
          color: #FEE8E8;

          .icon-arrow-down {
            color: #FEE8E8;
          }
        }
      }

      &:hover {
        background-color: #0000000a;
      }
    }
  }

  .icon-user {
    color: #0066FF;
    padding: 14px;
    font-size: 19px;
    background-color: #E5EFFF;
    border-radius: 50%;
  }

  .user_name {
    white-space: nowrap;
  }

  .icon-arrow-down {
    font-size: 11px;
    color: #9B9B9B;
    transition: transform 0.3s ease-in-out;
  }

  .show {
    .icon-arrow-down {
      transform: rotate(90deg);
    }
  }
}
</style>