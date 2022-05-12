<template>
  <Card class="product">
    <div class="product-img">
      <div class="wrapper d-flex justify-content-center align-items-center">
        <img src="../assets/img/product-5.png" alt="product image">
      </div>
    </div>
    <div class="product-title">
      <span> باتری تقویت شده برای گوشی سامسونگ مدل نوت</span>
    </div>
    <div class="product-detail d-flex flex-row justify-content-between">
      <span class="info">mAhظرفیت 3220</span>
      <span class="discount">18% تخفیف</span>
    </div>
    <div class="product-discount"><span>390.000 تومان</span></div>
    <div class="product-footer d-flex flex-row justify-content-between">
      <div class="product-price"><span>320.000 تومان</span></div>
      <div class="more d-flex align-items-center">
        <span>جزییات بیشتر</span>
        <span class="icon-arrow-left"></span>
      </div>
    </div>
  </Card>
</template>

<script setup>
import Card from './Card.vue'
</script>
<style scoped lang="scss">
$item-spacing: 15px;
.product {
  background-color: white;
  border-radius: 10px;
  padding: 20px;
  cursor: pointer;
  transition: all 250ms ease-in-out;

  &:hover {
    transform: scale(1.01);
  }

  .product-img {
    padding-top: 100%;
    background-color: rgba(156, 156, 156, 0.1);
    border-radius: 10px;
    position: relative;

    .wrapper {
      left: 0;
      top: 0;
      right: 0;
      bottom: 0;
      position: absolute;

      img {
        width: 100%;
        max-height: 100%;
      }
    }
  }

  .product-title {
    margin-top: $item-spacing;
    text-align: justify;
    font-weight: 500;

    span {
      white-space: break-spaces;
      word-break: break-word;
    }
  }

  .product-detail {
    margin-top: $item-spacing;
    font-size: 12px;

    .discount {
      padding: 5px 10px;
      color: white;
      border-radius: 10px;
      background-color: #EF1E49;
    }

    .info {
      color: #FFB300;
      border-radius: 10px;
      padding: 5px 10px;
      background-color: #FFF7E5;
    }
  }

  .product-discount {
    margin-top: $item-spacing;
    font-size: 12px;
    text-decoration: line-through;
    color: #CCCCCC;
  }

  .product-footer {
    margin-top: $item-spacing - 15px;

    .product-price {
      font-weight: 600;
    }

    .more {
      color: #0066FF;
      column-gap: 5px;
      font-weight: 500;
      font-size: 13px;
      transition: all 250ms ease-in-out;

      &:hover {
        color: #003b99;
      }

      &:hover .icon-arrow-left {
        transform: translateX(-2px);
      }

      .icon-arrow-left {
        transition: all 250ms ease-in-out;
        font-size: 14px;
      }
    }
  }
}
</style>