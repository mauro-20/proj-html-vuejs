<template>
  <section class="socials">
    <Twitter />
    <Instagram />
  </section>
</template>

<script>
  import Instagram from './Instagram.vue'
  import Twitter from './Twitters.vue'

  export default {
    name: 'Socials',
    components: {
      Twitter,
      Instagram
    }
  }
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  .socials{
    width: 30%;
    padding-left: 30px;
  }

</style>