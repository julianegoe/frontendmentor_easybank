<template>
<div class="about-item">
  <Icon  class="about-icon" :icon="icon"></Icon>
  <h3>{{aboutHeadline}}</h3>
  <p><slot></slot></p>
</div>
</template>

<script>
import Icon from '@/components/Icon.vue';

export default {
  name: 'AboutItem',
  components: {
    Icon,
  },
  props: {
    icon: String,
    aboutHeadline: String,
    aboutText: String,
  },
};
</script>

<style lang="scss" scoped>
@use '../assets/globals.scss' as *;

.about-item {
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    align-items: flex-start;

    > .about-icon {
        margin-bottom: $space-m;
    }
}
</style>
