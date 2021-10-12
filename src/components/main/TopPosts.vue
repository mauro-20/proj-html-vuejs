<template>
  <section class="top-posts">
    <div class="container">
      <div class="col">
        <h3 class="title">popular posts</h3>
          <ul>
            <li v-for="(post, index) in popular" :key="index" class="post">
              <SmallThumb :post="post"/>
            </li>
          </ul>
      </div>
      <div class="col">
        <h3 class="title">recent posts</h3>
        <ul>
          <li v-for="(post, index) in recent" :key="index" class="post">
            <SmallThumb :post="post"/>
          </li>
        </ul>
      </div>
      <div class="col">
        <h3 class="title">featured posts</h3>
        <HeroCard :post="featured" class="featured-posts"/>
        <h3 class="title featured-author">featured author</h3>
        <AuthorThumb :details="featuredAuthor"/>
      </div>
    </div>
  </section>
</template>

<script>
  import SmallThumb from './SmallThumb.vue';
  import HeroCard from './HeroCard.vue';
  import AuthorThumb from './AuthorThumb.vue';

  export default {
    name: 'TopPosts',
    components: {
      SmallThumb,
      HeroCard,
      AuthorThumb
    },
    props: {
      popular: Array,
      recent: Array,
      featured: Object,
      featuredAuthor: Object
    }
  }
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  .top-posts{
    background-color: $bg-light-100;

    .container{
      display: flex;
      padding: 50px 0;

      .col{
        width: calc((100% - 30px) / 3);
        margin-right: 15px;

        &:nth-child(3n){
          margin-right: 0;
        }

        .title{
          text-transform: uppercase;
          margin-bottom: 5px;
        }
        .post{
          border-bottom: 1px dotted $text-light-200;
          &:last-child{
            border: none;
          }
        }
        .featured-posts{
          margin: 40px 0 35px;
        }
      }
    }
  }

</style>