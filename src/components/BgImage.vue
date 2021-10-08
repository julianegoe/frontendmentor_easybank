<template>
<div class="bg-image">
    <slot></slot>
</div>
</template>

<script>
export default {
  name: 'BgImage',
  props: {
    imgPath: String,
  },
};
</script>

<style lang="scss" scoped>
@use '../assets/globals.scss' as *;

.bg-image {
    @include background('../assets/bg-intro-desktop.svg');

    @media ($breakpoint-small) {
        @include background('../assets/bg-intro-mobile.svg');
    }
}

</style>
