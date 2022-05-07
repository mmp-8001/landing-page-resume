<template>
  <Card class="results">
    <div class="recent-search d-flex flex-wrap">
      <a href="#" class="item" v-for="item of recentSearch" :title="item.title" :key="item.id">{{ item.title }}</a>
    </div>
    <div class="search-info d-flex">
      <span class="res-intro"> نتایج جستوجو برای </span>
      &nbsp;
      <span class="res-title flex-grow-1">باتری سامسونگ</span>
      <span class="res-count">{{ searchResults.length }} مورد</span>
    </div>
    <div class="search-result d-flex flex-column">
      <a href="#" v-for="result of searchResults" :key="result.id" class="result d-flex align-items-center"
         :title="result.title">
        <div class="img"><img :src="result.img" alt="product"></div>
        <div class="title flex-grow-1">{{ result.title }}</div>
        <span class="icon-arrow-down angle-left"></span>
      </a>
    </div>
    <div class="overlay">&nbsp;</div>
    <div class="prof-search"><span>جستجوی پیشرفته</span></div>
  </Card>
</template>

<script setup>
import {ref} from 'vue'
import Card from './Card.vue'

// Search results
const searchResults = ref([{
  id: 1,
  title: '9 Xiaomi Redmi Note باتری شیائومی',
  img: 'src/assets/img/product-1.png'
}, {
  id: 2,
  title: '9 Xiaomi Redmi Note باتری شیائومی',
  img: 'src/assets/img/product-1.png'
}, {
  id: 3,
  title: '9 Xiaomi Redmi Note باتری شیائومی',
  img: 'src/assets/img/product-1.png'
}, {
  id: 4,
  title: '9 Xiaomi Redmi Note باتری شیائومی',
  img: 'src/assets/img/product-1.png'
}, {
  id: 5,
  title: '9 Xiaomi Redmi Note باتری شیائومی',
  img: 'src/assets/img/product-1.png'
}, {
  id: 6,
  title: '9 Xiaomi Redmi Note باتری شیائومی',
  img: 'src/assets/img/product-1.png'
}, {
  id: 7,
  title: '9 Xiaomi Redmi Note باتری شیائومی',
  img: 'src/assets/img/product-1.png'
}])

// Recent search
const recentSearch = ref([{id: 1, title: "سامسونگ A12"}, {id: 2, title: "آیفون 12 پرو مکسA12"}, {
  id: 3,
  title: "شیائومی ردمی 9 اس"
}, {id: 4, title: "شیائومی ردمی 9 اس"}])

</script>

<style scoped lang="scss">
$corner-space: 18px;
$overlay-height: 25px;

.results {
  color: #9B9B9B;
  font-size: 13px;
  width: 100%;
  height: auto;
  right: 0;
  position: absolute;
  padding: $corner-space;
  top: calc(100% + 20px);

  .recent-search {
    column-gap: 5px;
    row-gap: 5px;

    .item {
      transition: all 250ms ease-in-out;
      padding: 5px 10px;
      overflow: hidden;
      text-overflow: ellipsis;
      border-radius: 40px;
      background-color: #EBEBEB;

      &:hover {
        background-color: #424242;
        color: #EBEBEB;
      }
    }
  }

  .search-info {
    margin-top: $corner-space;
    font-weight: 500;

    .res-title {
      width: 30%;
      overflow: hidden;
      text-overflow: ellipsis;
      color: #0D0D0D;
    }
  }

  .search-result {
    direction: ltr;
    height: 200px;
    margin-top: $corner-space;
    overflow-y: auto;
    padding-right: 5px;
    row-gap: 10px;

    .angle-left {
      transform: rotate(90deg);
    }

    .result {
      direction: rtl;
      column-gap: 10px;
      padding: 10px;
      border-radius: 5px;
      transition: all 250ms ease-in-out;

      &:hover {
        background-color: rgba(0, 0, 0, 0.039);
      }

      .title {
        width: 85%;
        overflow: hidden;
        text-overflow: ellipsis;
      }

      .img {
        width: 35px;
        height: 35px;

        img {
          width: 100%;
          max-height: 100%;
          padding: 3px;
          border: 2px solid #CCCCCC;
          border-radius: 5px;
        }
      }
    }
  }

  .prof-search {
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

  .overlay {
    background: linear-gradient(0deg, white, transparent);
    height: $overlay-height;
    margin-top: -$overlay-height;
  }
}
</style>