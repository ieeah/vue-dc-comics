<template>
  <div id="app">
    <div class="container">
      <Header />
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue';

export default {
  name: 'App',
  components: {
    Header,
  },
}
</script>

<style lang="scss">
@import '@/styles/globals.scss';
@import '@/styles/utilities.scss';
@import '@/styles/vars.scss';

</style>
