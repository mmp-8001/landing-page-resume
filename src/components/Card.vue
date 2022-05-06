<template>
  <div class="card">
    <slot></slot>
  </div>
</template>

<script setup>
</script>

<style scoped lang="scss">

.card {
  width: 100px;
  height: 100px;
  border-radius: 10px;
  box-shadow: 0 3px 20px rgba(0, 0, 0, 0.08);
}
</style>