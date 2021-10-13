<template>
  <section class="posts-preview">
    <ul>
      <li v-for="(post, index) in posts" :key="index">
        <PostPreview :post="post"/>
      </li>
    </ul>
  </section>
</template>

<script>
  import PostPreview from './PostPreview.vue'

  export default {
    name: 'PostsPreview',
    components: {
      PostPreview
    },
    props: {
      width: Number,
      posts: Array
    }
  }
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  .posts-preview{
    width: 80%;
  }
  

</style>