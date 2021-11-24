<template>
  <div id="app">
      <Header />
      <main>
        <Main_Section />
      </main>
      <Shopbar />
      <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Main_Section from './components/Main_Section.vue';
import Footer from './components/Footer.vue';
import Shopbar from './components/Shopbar.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main_Section,
    Footer,
    Shopbar,
  },
}
</script>

<style lang="scss">
@import '@/styles/globals.scss';
@import '@/styles/utilities.scss';
@import '@/styles/vars.scss';

</style>
