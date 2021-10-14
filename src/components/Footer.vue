<template>
  <footer>
    <div class="footer-top">
      <div class="container">
        <div class="col-400">
          <h5>ABOUT THE BLOG</h5>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tempore soluta delectus nihil.</p>
          <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Cupiditate sunt.</p>
          <h5 class="cursor">VIEW MORE ></h5>
        </div>
        <div class="col-300">
          <h5>RECENT POSTS</h5>
          <ul>
            <li v-for="(post,index) in recentPosts" :key="index" >
              <Post :post="post" />
            </li>
          </ul>
        </div>
        <div class="col-300">
          <h5>RECENT COMMENTS</h5>
          <ul>
            <li v-for="(comment, index) in recentComments" :key="index">
              <Comment :comment="comment" />
            </li>
          </ul>
        </div>
        <div class="col-200">
          <h5>CATEGORIES</h5>
          <ul>
            <li v-for="(category, index) in categories" :key="index" class="tags">
              <Category :category="category" />
            </li>
          </ul>
        </div>
      </div>
    </div>
    <div class="footer-bottom">
      <div class="container">
        
      </div>
    </div>
  </footer>
</template>

<script>
  import Post from './footer/Post.vue'
  import Comment from './footer/Comment.vue'
  import Category from './footer/Category.vue'

  export default {
    name: 'Footer',
    components: {
      Post,
      Comment,
      Category
    },
    data() {
      return {
        recentPosts: [
          {
            url: require("../assets/images/our-office-4-square.jpg"),
            content:
              "Lorem ipsum dolor sit consectetur adipisicing elit.",
            date: "12:53 AM Dec 19th",
          },
          {
            url: require("../assets/images/our-office-5-square.jpg"),
            content:
              "Lorem ipsum dolor sit consectetur adipisicing elit.",
            date: "12:53 AM Dec 19th",
          },
        ],
        recentComments: [
          {
            user: 'John Doe',
            post: 'Lorem ipsum dolor sit amet.',
            date: '12:55 AM Dec 19th'
          },
          {
            user: 'John Doe',
            post: 'Lorem ipsum dolor sit amet.',
            date: '12:55 AM Dec 19th'
          }
        ],
        categories: [
          'gadgets', 'photography', 'lifestyle', 'fashion', 'recipes', 'travel', 'business', 'architecture', 'reviews', 'sports', 'videos', 'technology', 'design'
        ]
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import '../assets/style/variables';

  .footer-top{
    padding: 80px 0 100px;
    background-color: $bg-dark-700;

    .container{
      display: flex;
      justify-content: space-between;
      .col-400{
        width: 410px;
      }
      .col-300{
        width: 340px;
        margin-right: 20px;
      }
      .col-200{
        width: 250px;
      }
      h5,
      h6{
        margin-bottom: 1.25rem;
        color: $text-light-100;
      }
      p{
        margin: 1.25rem 0;
        color: $text-dark-500;
        line-height: 2rem;
      }
      .cursor{
        cursor: pointer;
      }
      .tags{
        display: inline-block;
      }
    }
  }

  .footer-bottom{
    padding: 30px 0;
    background-color: $bg-dark-800;
  }

</style>