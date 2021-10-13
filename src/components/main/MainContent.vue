<template>
  <section>
    <div class="container">
      <PostsPreview :posts="posts"/>
      <Socials />
    </div>
  </section>
</template>

<script>
  import PostsPreview from "./PostsPreview.vue";
  import Socials from "./Socials.vue";

  export default {
    name: 'MainContent',
    components: {
      PostsPreview,
      Socials
    },
    props: {
      posts: Array
    }
  }
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  section{
    background-color: $bg-light-100;

    .container{
      display: flex;
      padding: 60px 0;
    }
  }

</style>