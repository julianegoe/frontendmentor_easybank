<template>
  <div class="layout">
      <slot></slot>
  </div>
</template>

<script>
export default {
  name: 'Layout',
  data() {
    return {
    };
  },
};
</script>

<style lang="scss" scoped>
@use '../assets/globals.scss' as *;

.layout {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    box-sizing: border-box;
    margin: $space-m;
    display: flex;
    flex-direction: column;
}

</style>
