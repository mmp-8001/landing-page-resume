<template>
  <div class="container">
    <div class="row">
      <div class="banner">
        <div
            class="content d-flex flex-md-row justify-content-md-between flex-column justify-content-center align-items-center"
            style="background-image: url('src/assets/img/banner.png')">
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
$vertical-space: 40px;

.banner {
  font-weight: 500;
  margin-bottom: $vertical-space;

  .content {
    cursor: pointer;
    color: white;
    border-radius: 10px;
    row-gap: 20px;
    background-repeat: no-repeat;
    background-size: cover;
    background-position: 50% 65%;
    padding: 30px 45px;

    &:hover .link .icon-arrow-left {
      transform: translateX(-3px);
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