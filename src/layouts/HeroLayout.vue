<template>
    <div class="hero-container">
        <slot name="hero-image"></slot>
        <slot name="hero-content"></slot>
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
    display: grid;
    grid-template-columns: 30% 70%;

    @media ($breakpoint-small) {
        grid-template-columns: 1fr;
    }
}

</style>
