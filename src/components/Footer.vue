<template>
  <footer class="footer-container">
    <Icon class="footer-logo" icon="logo"></Icon>
    <div class="footer-socialmedia">
      <Icon icon="icon-facebook"></Icon>
      <Icon icon="icon-youtube"></Icon>
      <Icon icon="icon-twitter"></Icon>
      <Icon icon="icon-pinterest"></Icon>
      <Icon icon="icon-instagram"></Icon>
    </div>
      <ul class="footer-links">
        <li>About Us</li>
        <li>Contact</li>
        <li>Blog</li>
        <li>Careers</li>
        <li>Support</li>
        <li>Privacy Policy</li>
      </ul>
    <button>Request Invite</button>
    <p>© Easybank. All Rights Reserved</p>
  </footer>
</template>

<script>
import Icon from '@/components/Icon.vue';

export default {
  name: 'Footer',
  components: {
    Icon,
  },
};
</script>

<style lang="scss" scoped>
@use '../assets/globals.scss' as *;

.footer-container {
  padding: $space-l $space-xxl $space-l $space-xxl;
  color: $color-very-light-grey;
  background: $color-dark-blue;
  display: grid;

  .footer-socialmedia {
    display: flex;
    flex-direction: row;

    > div {
      padding: $space-xs;
    }
  }

  .footer-links {
    padding: 0;
    > li {
      @include vertical-nav($space-s);
    }
  }

  @media ($breakpoint-small) {
    padding: $space-xl $space-xl $space-m $space-xl;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    row-gap: $space-l;
  }
}

:deep(svg > g > path) {
  fill: $color-white;
}

</style>
