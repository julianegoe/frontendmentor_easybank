<template>
<h2>Latest Articles</h2>
 <div class="blog-container">
     <slot></slot>
 </div>
</template>

<script>
export default {
  name: 'BlogLayout',
  components: {
  },
};
</script>

<style lang="scss" scoped>
@use '../assets/globals.scss' as *;

h2 {
    padding: $space-l $space-xxl $space-l $space-xxl;
    background: $color-very-light-grey;
    margin: 0;

    @media ($breakpoint-small) {
        padding: $space-m $space-xl $space-m $space-xl;

    }
    }

.blog-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    grid-gap: $space-m;
    padding: $space-l $space-xxl $space-l $space-xxl;
    background: $color-very-light-grey;

    @media ($breakpoint-small) {
       grid-template-columns: 1fr;
       padding: $space-m $space-xl $space-m $space-xl;
    }
}

</style>
