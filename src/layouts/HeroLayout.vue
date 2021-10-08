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

    @media ($breakpoint-small) {
        flex-direction: column;
        position: absolute;
        top: -90px;
    }
}

</style>
