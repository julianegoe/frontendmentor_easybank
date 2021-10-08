<template>
  <div class="icon" v-html="loadedIcon.default"/>
</template>

<script>
export default {
  name: 'Icon',
  props: {
    icon: {
      type: String,
      required: true,
    },
  },
  data() {
    return {
      loadedIcon: '',
    };
  },
  mounted() {
    // eslint-disable-next-line
    this.loadedIcon = require(`!!raw-loader!@/assets/${this.icon}.svg`);
  },
};
</script>

<style lang="scss" scoped>

</style>
