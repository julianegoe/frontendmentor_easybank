<template>
  <box>
      <img class="article-image" :src="imageName" />
      <div class="article-preview">
          <div>By {{author}}</div>
          <h3>{{headline}}</h3>
          <p>
              <slot></slot>
          </p>
      </div>
  </box>
</template>

<script>
import Box from './Box.vue';

export default {
  components: { Box },
  name: 'BlogArticle',
  props: {
    name: String,
    author: String,
    headline: String,
    teaser: String,
  },
  computed: {
    imageName() {
    // eslint-disable-next-line
      const imageName = require(`../assets/image-${this.name}.jpg`);
      return imageName;
    },
  },
};
</script>

<style lang="scss" scoped>
@use '../assets/globals.scss' as *;

.article-image {
    width: 100%;
    height: auto;
    object-fit: cover;
}

</style>
