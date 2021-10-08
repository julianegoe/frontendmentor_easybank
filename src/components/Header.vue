<template>

<!-- Desktop Header -->
<header>
    <nav class="nav">
        <img src="../assets/logo.svg" alt="Logo Easybank" />
        <icon class="nav-hamburger" icon="icon-hamburger"></icon>
        <ul class="nav-links desktop">
            <li>Home</li>
            <li>About</li>
            <li>Contact</li>
            <li>Blog</li>
            <li>Careers</li>
        </ul>
        <button class="call-to-action desktop">Request Invite</button>
    </nav>
</header>

<!-- Mobile Header -->
</template>

<script>
import Icon from '@/components/Icon.vue';

export default {
  name: 'MobileNav',
  components: {
    Icon,
  },
  data() {
    return {
    };
  },
};
</script>

<style lang="scss" scoped>
@use '../assets/globals.scss' as *;

header {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    min-height: $space-xxl;
    background: $color-white;
    z-index: $z-index-nav;

    .nav {
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
        padding: $space-m;

        .nav-links.desktop {
            display: flex;
            justify-content: center;
            padding: 0;

            @media ($breakpoint-small) {
                display: none;
            }

          > li {
              @include horizontal-nav;
              color: $color-greyish-blue;
            }
        }

        .call-to-action.desktop {
            @media ($breakpoint-small) {
                display: none;
            }
        }
        .nav-hamburger {
            display: none;

            @media ($breakpoint-small) {
                display: initial;
            }
        }
    }
}
</style>
