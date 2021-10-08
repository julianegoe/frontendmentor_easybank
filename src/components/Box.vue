<template>
  <div class="box">
      <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'MobileNav',
  data() {
    return {
    };
  },
};
</script>

<style lang="scss" scoped>
@use '../assets/globals.scss' as *;

.box {
    border-radius: $border-radius-box;
    background: $color-white;
}

</style>
