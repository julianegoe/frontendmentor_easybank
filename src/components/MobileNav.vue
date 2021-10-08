<template>
<box class="nav-container">
      <ul>
          <li>Home</li>
          <li>About</li>
          <li>Contact</li>
          <li>Blog</li>
          <li>Careers</li>
      </ul>
</box>
</template>

<script>
import Box from '@/components/Box.vue';

export default {
  name: 'MobileNav',
  components: {
    Box,
  },
  data() {
    return {
    };
  },
};
</script>

<style lang="scss" scoped>
@use '../assets/globals.scss' as *;

.nav-container {
    z-index: $z-index-nav;

    ul {
    padding-left: 0;
    margin: 0;

    > li {
    @include vertical-nav($space-m)
    }
}
}

</style>
