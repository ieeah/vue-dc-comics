<template>
  <div id="app">
      <Header />
      <main>
        <MainSection />
        <Merchbar />
      </main>
      <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue';
import MainSection from './components/MainSection.vue';
import Footer from './components/Footer.vue';
import Merchbar from '@/components/Merchbar.vue';

export default {
  name: 'App',
  components: {
    Header,
    MainSection,
    Footer,
    Merchbar,
  },
}
</script>

<style lang="scss">
@import '@/styles/globals.scss';
@import '@/styles/utilities.scss';
@import '@/styles/vars.scss';

</style>
