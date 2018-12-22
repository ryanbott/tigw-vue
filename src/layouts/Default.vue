<template lang="pug">
  <div class="layout">
    <Header />
    <slot/>
  </div>
</template>

<script>
import config from '~/.temp/config.js';
import Header from '~/components/Header.vue';

export default {
  components: {
    Header
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
