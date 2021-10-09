<template>
 <div class="about-container">
     <div class="about-headline">
        <h2>Why choose Easybank?</h2>
        <p>We leverage Open Banking to turn your bank account into your financial hub.
          Control your finances like never before.</p>
      </div>
     <slot></slot>
 </div>
</template>

<script>
export default {
  name: 'HeroLayout',
  components: {
  },
};
</script>

<style lang="scss" scoped>
@use '../assets/globals.scss' as *;

.about-container {
 display: grid;
 grid-template-columns: repeat(4, 1fr);
 grid-template-rows: auto auto;
 grid-gap: $space-l;
 padding: $space-l $space-xxl $space-l $space-xxl;
 background: $color-light-greyish-blue;

 @media ($breakpoint-small) {
  grid-template-columns: 1fr;
  padding: $space-m $space-xl $space-m $space-xl;
 }

 .about-headline {
     grid-column: 1 / span 4;
     grid-row: 1 / span 1;

     @media ($breakpoint-small) {
         grid-column: span 1;
         grid-row: auto;
     }

     > p {
         width: 60%;

         @media ($breakpoint-small) {
             width: 100%;
             text-align: center;
         }
     }
     > h2 {
         @media ($breakpoint-small) {
             text-align: center;
         }
     }
 }
}
</style>
