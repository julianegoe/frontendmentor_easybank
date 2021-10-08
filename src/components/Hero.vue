<template>
    <img src="../assets/image-mockups.png" alt="iPhones"/>
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
    z-index: $z-index-hero;
    width: 50%;
    object-fit: cover;

    @media ($breakpoint-small) {
        width: 100%;
        order: 1;
        /* transform: translateY(-150px); */
    }
}

</style>
