<template>
    <div class="hero-container">
        <slot name="hero-content"></slot>
        <slot name="hero-image"></slot>
    </div>
</template>

<script>

export default {
  name: 'HeroLayout',
  components: {
  },
};
</script>

<style lang="scss" scoped>
@use '../assets/globals.scss' as *;

.hero-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    padding: $space-m;
    background: $color-very-light-grey;

    @include background('../assets/bg-intro-desktop.svg', 150% 5%, 70%);

    @media ($breakpoint-small) {
        @include background('../assets/bg-intro-mobile.svg', top right, contain);
        flex-direction: column;
        position: absolute;
    }
}

</style>
