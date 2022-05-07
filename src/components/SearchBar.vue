<template>
  <DropDown class="search d-flex flex-nowrap">
    <template #dropdown>
      <span class="icon-search"></span>
      <input @focus.stop="" id="search-bar" class="search-bar" type="text"
             placeholder="کالا یا کلمه مورد نظر  خود راتایپ کنید...">
    </template>
    <template #content>
      <SearchResult class="result d-flex flex-column"/>
    </template>
  </DropDown>
</template>

<script setup>
import DropDown from './DropDown.vue'
import SearchResult from './SearchResult.vue'

</script>

<style scoped lang="scss">
.search {
  position: relative;
  cursor: pointer;
  width: 100%;
  align-items: center;
  justify-content: center;
  column-gap: 15px;

  .icon-search {
    right: 15px;
    font-size: 20px;
    position: absolute;
  }

  .search-bar {
    padding: 9px 45px 9px 10px;
    font-size: 16px;
    outline: none;
    font-family: Yekan, Tahoma, sans-serif;
    width: 100%;
    cursor: pointer;
    border: 2px solid #EBEBEB;
    border-radius: 10px;
    transition: all 0.2s ease-in-out;

    &:hover, &:focus {
      border-color: rgba(12, 150, 187, 0.36);
      box-shadow: 0 0 12px 0 rgba(183, 239, 247, 0.64);
    }

    &::placeholder {
      opacity: 0.5;
    }
  }
}
</style>