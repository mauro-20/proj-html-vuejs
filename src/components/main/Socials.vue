<template>
  <section class="socials">
    <Twitter />
    <Instagram />
    <Facebook />
  </section>
</template>

<script>
  import Instagram from './Instagram.vue'
  import Twitter from './Twitters.vue'
  import Facebook from './Facebook.vue'

  export default {
    name: 'Socials',
    components: {
      Twitter,
      Instagram,
      Facebook
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