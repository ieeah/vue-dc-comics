<template>
  <div id="app">
      <Header />
      <main>
        <Main_Section />
      </main>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main_Section from './components/Main_Section.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main_Section,
  },
}
</script>

<style lang="scss">
@import '@/styles/globals.scss';
@import '@/styles/utilities.scss';
@import '@/styles/vars.scss';

</style>
