<template>
  <header>
    <HeaderTop />
    <HeaderBottom :logoUrl="logoUrl" :nav="nav"/>
  </header>
</template>

<script>
import HeaderTop from './header/HeaderTop.vue'
import HeaderBottom from './header/HeaderBottom.vue'

export default {
  name: 'Header',
  components: {
    HeaderTop,
    HeaderBottom
  },
  props: {
    logoUrl: String,
    nav: Array
  }
}
</script>

<style lang="scss" scoped>

</style>