<template>
  <div id="app">
    <Header :logoUrl="require('./assets/images/logo-default-slim.png')" :nav="mainNav"/>
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer
  },
  data() {
    return {
      mainNav: ['home', 'elements', 'features', 'pages', 'portfolio', 'blog', 'shop']
    }
  }
}
</script>

<style lang="scss">
  @import './assets/style/common';

</style>
