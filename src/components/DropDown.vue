<template>
  <div @click="show=true" :class="{'show':!show}" v-click-outside="onClickOutside">
    <slot name="dropdown"></slot>
    <Transition>
      <slot v-if="show" name="content"></slot>
    </Transition>
  </div>
</template>


<script>
import vClickOutside from "click-outside-vue3"

export default {
  data() {
    return {
      show: false
    }
  },
  directives: {
    clickOutside: vClickOutside.directive
  },
  methods: {
    onClickOutside(event) {
      if (this.show === true) this.show = false
    }
  }
};
</script>
<style scoped lang="scss">
.v-enter-active,
.v-leave-active {
  transition: all 0.3s ease-in-out;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
  transform: translateY(-30px);
}
</style>