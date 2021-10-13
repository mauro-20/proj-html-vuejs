<template>
  <section class="posts-preview">
    <ul>
      <li v-for="(post, index) in posts" :key="index">
        <PostPreview :post="post"/>
      </li>
    </ul>
    <nav class="nav-pages">
      <div class="btn-nav"><i class="fas fa-angle-left"></i></div>
      <div class="btn-nav active">1</div>
      <div class="btn-nav">2</div>
      <div class="btn-nav">3</div>
      <div class="btn-nav"><i class="fas fa-angle-right"></i></div>
    </nav>
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

    .nav-pages{
      display: flex;
      justify-content: flex-end;

      .btn-nav{
        height: 35px;
        width: 30px;
        border: 1px solid $bd-light-500;
        border-right: none;
        text-align: center;
        line-height: 35px;
        // font-size: 20px;
        color: $text-primary;
        cursor: pointer;

        &:last-child{
          border-right: 1px solid $bd-light-500;
        }
        &.active{
          color: $text-light-100;
          background-color: $bg-primary;
          border: 1px solid $bg-primary;
        }
      }
    }
  }
  

</style>