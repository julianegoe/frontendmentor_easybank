<template>
 <div class="hero-content">
  <h1>Next generation digital banking</h1>
  <p>
   Take your financial life online. Your Easybank account will be a
   one-stop-shop for spending, saving, budgeting, investing, and much more.
  </p>
  <button>Request invite</button>
 </div>
</template>

<script>
export default {
  name: 'HeroContent',
  components: {},
};
</script>

<style lang="scss" scoped>
@use '../assets/globals.scss' as *;

.hero-content {
    grid-column: 1 / span 1;
    width: 100%;
    height: 35rem;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: center;
    padding: 0 $space-xxl 0 $space-xxl;
    background: $color-very-light-grey;

    > h1 {
        text-align: left;
    }

    > p {
       text-align: justify;
       text-justify: inter-word;
       line-height: $line-height-paragraph;
    }

    @media ($breakpoint-small) {
        height: auto;
        padding: 0 0 $space-xxl 0;
        align-items: center;
        justify-content: flex-start;

        > h1 {
            text-align: center;
        }

        > p {
            padding: 0 $space-xl 0 $space-xl;
        }
    }
}
</style>
