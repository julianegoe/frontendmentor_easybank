<template>
  <Header></Header>
  <Layout>
    <!-- <mobile-nav class="mobile-nav__position"></mobile-nav> -->
    <hero-layout>
      <template v-slot:hero-content><hero-content></hero-content></template>
      <template v-slot:hero-image><Hero class="hero-image"></Hero></template>
    </hero-layout>
  </Layout>
</template>

<script>
/* import MobileNav from './components/MobileNav.vue'; */
import Header from '@/components/Header.vue';
import Layout from '@/layouts/AppLayout.vue';
import Hero from '@/components/Hero.vue';
import HeroContent from '@/components/HeroContent.vue';
import HeroLayout from '@/layouts/HeroLayout.vue';

export default {
  name: 'App',
  components: {
    Header,
    Layout,
    Hero,
    HeroContent,
    HeroLayout,
  },
};
</script>

<style lang="scss">
@use './assets/globals.scss' as *;

body {
    @include background('./assets/bg-intro-desktop.svg', 150% 5%, 70%);

    @media ($breakpoint-small) {
        @include background('./assets/bg-intro-mobile.svg', top, cover);
    }
}

.mobile-nav__position {
  position: relative;
  top: $space-xxl;
}

</style>
