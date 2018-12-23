<template lang="pug">
  <div class="layout">
    <Header />
    <Subscribe />
    <slot/>
  </div>
</template>

<script>
import config from '~/.temp/config.js';
import Header from '~/components/Header.vue';
import Subscribe from '~/components/Subscribe.vue';

export default {
  components: {
    Header,
    Subscribe,
  },
  computed: {
    titleTag () {
      return this.$route.name === 'home' ? 'h1' : 'h6'
    },
    config () {
      return config
    }
  }
}
</script>
