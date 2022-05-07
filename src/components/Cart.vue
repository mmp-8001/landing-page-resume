<template>
  <DropDown class="shop d-flex align-items-center justify-content-center">
    <template #dropdown>
      <span class="shop-count">3</span>
      <span class="icon-shopping-cart">
          <span class="path1"></span>
          <span class="path2"></span>
          <span class="path3"></span>
          <span class="path4"></span>
        </span>
    </template>
    <template #content>
      <Card class="cart">
        <div class="cart-info d-flex flex-nowrap justify-content-between">
          <span class="title">سبد خرید</span>
          <span class="count">2 مورد</span>
        </div>
        <div class="cart-content d-flex flex-column justify-content-start">
          <div class="product d-flex flex-column">
            <div class="title d-flex flex-nowrap">
              باتری تقویت شده برای گوشی ساموسنگ Note4
            </div>
            <div class="footer align-items-center d-flex flex-nowrap">
              <span class="price flex-grow-1">320.000 تومان</span>
              <div class="count align-items-center d-flex flex-nowrap">
                <span class="plus">+</span>
                <span class="num">2 عدد</span>
                <span class="minus">-</span>
              </div>
              <span class="icon-trash d-flex justify-content-center align-items-center"></span>
            </div>
          </div>
          <div class="product d-flex flex-column">
            <div class="title d-flex flex-nowrap">
              باتری تقویت شده برای گوشی ساموسنگ Note4
            </div>
            <div class="footer align-items-center d-flex flex-nowrap">
              <span class="price flex-grow-1">320.000 تومان</span>
              <div class="count align-items-center d-flex flex-nowrap">
                <span class="plus">+</span>
                <span class="num">2 عدد</span>
                <span class="minus">-</span>
              </div>
              <span class="icon-trash d-flex justify-content-center align-items-center"></span>
            </div>
          </div>
          <div class="product d-flex flex-column">
            <div class="title d-flex flex-nowrap">
              باتری تقویت شده برای گوشی ساموسنگ Note4
            </div>
            <div class="footer align-items-center d-flex flex-nowrap">
              <span class="price flex-grow-1">320.000 تومان</span>
              <div class="count align-items-center d-flex flex-nowrap">
                <span class="plus">+</span>
                <span class="num">2 عدد</span>
                <span class="minus">-</span>
              </div>
              <span class="icon-trash d-flex justify-content-center align-items-center"></span>
            </div>
          </div>
          <div class="product d-flex flex-column">
            <div class="title d-flex flex-nowrap">
              باتری تقویت شده برای گوشی ساموسنگ Note4
            </div>
            <div class="footer align-items-center d-flex flex-nowrap">
              <span class="price flex-grow-1">320.000 تومان</span>
              <div class="count align-items-center d-flex flex-nowrap">
                <span class="plus">+</span>
                <span class="num">2 عدد</span>
                <span class="minus">-</span>
              </div>
              <span class="icon-trash d-flex justify-content-center align-items-center"></span>
            </div>
          </div>
        </div>
        <div class="purchase"><span>خرید نهایی</span></div>
      </Card>
    </template>
  </DropDown>
</template>

<script setup>
import {ref} from 'vue'
import Card from './Card.vue'
import DropDown from './DropDown.vue'

// User Cart
const cart = ref([{
  id: 1,
  title: '9 Xiaomi Redmi Note باتری شیائومی',
  price: '320.000 تومان',
  count: '2 عدد'
}, {
  id: 2,
  title: '9 Xiaomi Redmi Note باتری شیائومی',
  price: '320.000 تومان',
  count: '2 عدد'
}, {
  id: 3,
  title: '9 Xiaomi Redmi Note باتری شیائومی',
  price: '320.000 تومان',
  count: '2 عدد'
}, {
  id: 4,
  title: '9 Xiaomi Redmi Note باتری شیائومی',
  price: '320.000 تومان',
  count: '2 عدد'
},])
</script>

<style scoped lang="scss">
$corner-space: 18px;

.shop {
  position: relative;
  justify-content: center;
  cursor: pointer;

  .shop-count {
    display: flex;
    justify-content: center;
    align-items: center;
    position: absolute;
    font-size: 15px;
    font-weight: 600;
    border-radius: 50%;
    background-color: #EF1E1E;
    color: white;
    width: 29px;
    height: 29px;
    top: 59%;
    left: 59%;
  }

  .icon-shopping-cart {
    font-size: 22px;
    padding: 10px;
    border: 2px solid #EBEBEB;
    border-radius: 10px;
  }
}

.cart {
  position: absolute;
  color: #9B9B9B;
  font-size: 13px;
  width: calc(100% + 175px);
  height: auto;
  right: 0;
  padding: $corner-space;
  top: calc(100% + 20px);

  .cart-info {
    font-weight: 500;
    margin-bottom: 10px;

    .title {
      color: #0D0D0D;
    }
  }

  .cart-content {
    direction: ltr;
    overflow-x: auto;
    height: 200px;
    margin-right: -8px;
    padding-right: 3px;

    .product {
      direction: rtl;
      position: relative;
      padding: 10px 0;

      &:not(:last-child):after {
        content: "";
        display: block;
        position: absolute;
        width: 100%;
        left: 0;
        bottom: 0;
        height: 1px;
        border-radius: 5px;
        background-color: rgba(204, 204, 204, 0.53);
      }

      .title {
        position: relative;
        white-space: pre-wrap;
        padding: 2px 8px 2px 0;

        &:after {
          display: block;
          position: absolute;
          right: 0;
          top: 0;
          height: 100%;
          width: 3px;
          border-radius: 20px;
          background-color: #0066FF;
          content: "";
        }
      }

      .footer {
        column-gap: 10px;
        font-weight: 500;

        .icon-trash {
          font-size: 15px;
          padding: 4px;
          background-color: #EBEBEB;
          border-radius: 5px;
          transition: all 250ms ease-in-out;

          &:hover {
            background-color: #EF1E1E;
            color: white;
          }
        }

        .price {
          color: #0D0D0D;
        }

        .count {
          column-gap: 5px;
        }

        .minus, .plus {
          transition: all 250ms ease-in-out;
          font-size: 20px;
        }

        .minus:hover {
          color: #EF1E1E;
        }

        .plus:hover {
          color: #6cd048;
        }
      }
    }
  }

  .purchase {
    transition: all 250ms ease-in-out;
    color: #0066FF;
    margin-top: $corner-space;
    text-align: center;
    padding: 6px;
    font-size: 16px;
    font-weight: 500;
    border: 2px solid #CCCCCC;
    border-radius: 10px;

    &:hover {
      background-color: #0066FF;
      border-color: #0066FF;
      color: white;
    }
  }
}
</style>