<template>
  <Header></Header>
  <Layout>
    <!-- <mobile-nav class="mobile-nav__position"></mobile-nav> -->
    <hero-layout>
      <template v-slot:hero-content><hero-content></hero-content></template>
      <template v-slot:hero-image><Hero class="hero-image"></Hero></template>
    </hero-layout>
    <about-layout>
  <about-item icon="icon-online" aboutHeadline="Online Banking">
   Our modern web and mobile applications allow you to keep track of your
   finances wherever you are in the world.
  </about-item>
  <about-item icon="icon-budgeting" aboutHeadline="Simple Budgeting">
   See exactly where your money goes each month. Receive notifications when
   you’re close to hitting your limits.
  </about-item>
  <about-item icon="icon-onboarding" aboutHeadline="Fast Onboarding">
   We don’t do branches. Open your account in minutes online and start taking
   control of your finances right away.
  </about-item>
  <about-item icon="icon-api" aboutHeadline="Open API">
   Manage your savings, investments, pension, and much more from one account.
   Tracking your money has never been easier.
  </about-item>
    </about-layout>
  </Layout>
</template>

<script>
/* import MobileNav from './components/MobileNav.vue'; */
import Header from '@/components/Header.vue';
import Layout from '@/layouts/AppLayout.vue';
import Hero from '@/components/Hero.vue';
import HeroContent from '@/components/HeroContent.vue';
import HeroLayout from '@/layouts/HeroLayout.vue';
import AboutLayout from '@/layouts/AboutLayout.vue';
import AboutItem from '@/components/AboutItem.vue';

export default {
  name: 'App',
  components: {
    Header,
    Layout,
    Hero,
    HeroContent,
    HeroLayout,
    AboutLayout,
    AboutItem,
  },
};
</script>

<style lang="scss">
@use './assets/globals.scss' as *;

body {
  @include background('./assets/bg-intro-desktop.svg', 150% 15%, 70%);
  background-blend-mode: normal;
  background-color: $color-very-light-grey;

  @media ($breakpoint-small) {
    @include background('./assets/bg-intro-mobile.svg', top right, contain);
  }
}

.mobile-nav__position {
  position: relative;
  top: $space-xxl;
}

</style>
