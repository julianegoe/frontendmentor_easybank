<template>
  <Header></Header>
  <Layout>
    <!-- <mobile-nav class="mobile-nav__position"></mobile-nav> -->
    <Hero class="hero-image desktop"></Hero>
    <hero-layout>
      <template v-slot:hero-image><Hero class="hero-image smartphone"></Hero></template>
      <template v-slot:hero-content><hero-content></hero-content></template>
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
  <blog-layout>
    <blog-article
    name="currency" author="Claire Robinson" headline="Receive money in any currency with no fees">
      The world is getting smaller and we’re becoming more mobile.
      So why should you be forced to only receive money in a single …
    </blog-article>

    <blog-article
    name="restaurant" author="Wilson Hutton" headline="Treat yourself without worrying about money">
      Our simple budgeting feature allows you to separate out
      your spending and set realistic limits each month. That means you …
    </blog-article>

    <blog-article
    name="plane" author="Wilson Hutton" headline="Take your Easybank card wherever you go">
      We want you to enjoy your travels.
      This is why we don’t charge any fees on purchases while you’re abroad. We’ll even show you …
    </blog-article>

    <blog-article
    name="confetti" author="Claire Robinson" headline="Our invite-only Beta accounts are now live!">
      After a lot of hard work by the whole team, we’re excited to launch our closed beta.
      It’s easy to request an invite through the site ...
    </blog-article>
  </blog-layout>
  <Footer></Footer>
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
import BlogLayout from '@/layouts/BlogLayout.vue';
import BlogArticle from '@/components/BlogArticle.vue';
import Footer from './components/Footer.vue';

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
    BlogLayout,
    BlogArticle,
    Footer,
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
    @include background('./assets/bg-intro-mobile.svg', top center, cover);
  }
}

.hero-image.smartphone {
  display: none;
}

@media ($breakpoint-small) {
  .hero-image.smartphone {
    display: initial;
  }

  .hero-image.desktop {
    display: none;
  }
}

.mobile-nav__position {
  position: relative;
  top: $space-xxl;
}

</style>
