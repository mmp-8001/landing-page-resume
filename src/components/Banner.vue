<template>
  <div class="container">
    <div class="row">
      <div class="banner">
        <div class="content d-flex justify-content-between" style="background-image: url('src/assets/img/banner.png')">
          <div class="title"><span>جشنواره تابستانه استارموبو با جوایز و تخفیف ویژه</span></div>
          <div class="link d-flex align-items-center">
            <span>صفحه جشنواره</span>
            <span class="icon-arrow-left"></span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>

</script>

<style scoped lang="scss">
.banner {
  font-weight: 500;

  .content {
    cursor: pointer;
    color: white;
    background-color: red;
    border-radius: 10px;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 50% 65%;
    padding: 30px 45px;

    &:hover .link .icon-arrow-left {
      transform: translateX(-3px);
    }

    .title {

    }

    .link {
      column-gap: 10px;

      .icon-arrow-left {
        transition: all 250ms ease-in-out;
      }
    }
  }
}
</style>