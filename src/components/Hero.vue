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
    position: relative;
    width: 50%;
    object-fit: contain;
    left: 10%;

    @media ($breakpoint-small) {
        width: 100%;
        order: 1;
    }
}

</style>
