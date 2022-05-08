<template>
  <div class="collapsible">
    <div class="header d-flex column-gap flex-nowrap align-items-center menu-item" @click="collapse" ref="header">
      <slot name="header"></slot>
      <span class="icon-arrow-left"></span>
    </div>
    <div class="content d-flex flex-column">
      <slot name="content"></slot>
    </div>
  </div>
</template>

<script setup>
import {ref} from "vue";

const header = ref(null)

// Collapse function
function collapse() {
  let content = header.value.nextElementSibling;
  let children = content.querySelectorAll(".content");
  if (content.style.maxHeight) {
    header.value.classList.remove('expanded')
    content.style.maxHeight = null;
    children.forEach(value => {
      value.style.maxHeight = null
      value.previousSibling.classList.remove('expanded')
    });
  } else {
    header.value.classList.add('expanded')
    let childrenHeight = Array.from(children).reduce((accumulator, currentValue) => accumulator + currentValue.scrollHeight, 0);
    content.style.maxHeight = (content.scrollHeight + childrenHeight) + "px";
  }
}
</script>

<style scoped lang="scss">
$divider-color: rgb(49, 61, 80);
$icon-spacing: 10px;
$primary-color: white;
$secondary-color: #9b9b9b;

.collapsible {
  width: 100%;

  .header {
    cursor: pointer;
    column-gap: $icon-spacing;
    overflow: hidden;
    margin: 12px 0;

    .icon-arrow-left {
      transition: all 250ms ease-in-out;
    }

    &.expanded .icon-arrow-left {
      transform: rotate(-90deg);
    }
  }

  .content {
    padding-right: 37px;
    overflow: hidden;
    row-gap: 20px;
    font-size: 14px;
    max-height: 0;
    transition: max-height 250ms ease-in-out;
    position: relative;

    &:before {
      position: absolute;
      content: "";
      width: 3px;
      border-radius: 10px;
      height: 100%;
      background-color: $divider-color;
      right: 0;
      top: 0;
      margin-right: 6px;
      display: block;
    }
  }
}
</style>