<template>
    <img class="hero-image" src="../assets/image-mockups.png" alt="iPhones"/>
</template>

<script>

export default {
  name: 'Hero',
  components: {
  },
};
</script>

<style lang="scss" scoped>
@use '../assets/globals.scss' as *;

.hero-image {
    position: absolute;
    top: -$space-l;
    right: -$space-xxl;
    max-width: 50%;
    object-fit: scale-down;

    @media ($breakpoint-small) {
        position: inherit;
        width: 100%;
        object-fit: cover;
    }
}

</style>
