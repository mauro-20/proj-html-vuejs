<template>
  <main>
    <Hero :posts="heroPosts" />
    <TopPosts :popular="popularPosts" :recent="recentPosts" :featured="featuredPost" :featuredAuthor="featuredAuthor"/>
    <TagMenu :tags="tags"/>
    <MainContent :posts="previewPosts" />
  </main>
</template>

<script>
import Hero from "./main/Hero.vue";
import TopPosts from "./main/TopPosts.vue";
import TagMenu from "./main/TagMenu.vue";
import MainContent from "./main/MainContent.vue";

export default {
  name: "Main",
  components: {
    Hero,
    TopPosts,
    TagMenu,
    MainContent
  },
  data() {
    return {
      heroPosts: [
        {
          url: require("../assets/images/blog-46.jpg"),
          title: "how to take better concert picture in 30 seconds",
          tag: "photography",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
        },
        {
          url: require("../assets/images/blog-47.jpg"),
          title: "gadgets that make your smartphone even smarter",
          tag: "gadgets",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
        },
        {
          url: require("../assets/images/blog-48.jpg"),
          title: "20 top-rated tourist attractions in manhattan",
          tag: "travel",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
        },
        {
          url: require("../assets/images/blog-49.jpg"),
          title: "the best way to ride a motorcycle",
          tag: "lifstyle",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
        },
        {
          url: require("../assets/images/blog-50.jpg"),
          title: "5 fun things to do at the beach",
          tag: "travel",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
        },
        {
          url: require("../assets/images/blog-51.jpg"),
          title: "amazingly fresh fruit and herbs drinks for summer",
          tag: "recipes",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
        },
      ],
      popularPosts: [
        {
          url: require("../assets/images/blog-55.jpg"),
          title: "Simple Ways to Have a Pretty Face",
          tag: "lifestyle",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
          date: "January 12, 2019",
        },
        {
          url: require("../assets/images/blog-56.jpg"),
          title: "Ranking the greatest players in basketball",
          tag: "sport",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
          date: "January 12, 2019",
        },
        {
          url: require("../assets/images/blog-57.jpg"),
          title: "4 Ways to Look Cool in Glasses",
          tag: "photography",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
          date: "January 12, 2019",
        },
        {
          url: require("../assets/images/blog-58.jpg"),
          title: "Top Camper Trailer Towing Tips",
          tag: "travel",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
          date: "January 12, 2019",
        },
        {
          url: require("../assets/images/blog-59.jpg"),
          title: "5 Lovely Walks in New York",
          tag: "travel",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
          date: "January 12, 2019",
        },
      ],
      recentPosts: [
        {
          url: require("../assets/images/blog-65.jpg"),
          title: "Main Reasons To Stop Texting And Driving",
          tag: "lifestyle",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
          date: "January 12, 2019",
        },
        {
          url: require("../assets/images/blog-66.jpg"),
          title: "Tips to Help You Quickly Prepare your Lunch",
          tag: "recipe",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
          date: "January 12, 2019",
        },
        {
          url: require("../assets/images/blog-67.jpg"),
          title: "Why should I buy a smartwatch",
          tag: "tech",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
          date: "January 12, 2019",
        },
        {
          url: require("../assets/images/blog-68.jpg"),
          title: "The best augmented reality smartglasses",
          tag: "tech",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
          date: "January 12, 2019",
        },
        {
          url: require("../assets/images/blog-69.jpg"),
          title: "12 Helthiest Foods to Eat for Breakfast",
          tag: "recipe",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
          date: "January 12, 2019",
        },
      ],
      featuredPost: {
        url: require("../assets/images/blog-66.jpg"),
        title: "Tips to Help You Quickly Prepare your Lunch",
        tag: "recipe",
        content:
          "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
        date: "January 12, 2019",
      },
      featuredAuthor: {
        url: require("../assets/images/avatar.jpg"),
        name: 'John Doe',
        info: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Ipsum dolor sit amet, consectetur adipisicing elit.'
      },
      tags: [
        'gadgets', 'photography', 'lifestyle', 'fashion', 'recipes', 'travel'
        ],
      previewPosts :[
        {
          url: require("../assets/images/blog-54.jpg"),
          title: "How to Make Friends as a Grown-Up",
          tags: ['Lifestyle,', 'Travel'],
          author: "John Doe",
          commentNumber: "12",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
          date: "January 12, 2019",
        },
        {
          url: require("../assets/images/blog-55 (1).jpg"),
          title: "Simple Ways to Have a Pretty Face",
          tags: ['Photography,', 'Travel'],
          author: "John Doe",
          commentNumber: "12",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
          date: "January 12, 2019",
        },
        {
          url: require("../assets/images/blog-56 (1).jpg"),
          title: "Ranking the greatest players in basketball",
          tags: ['Sports,', 'Business'],
          author: "John Doe",
          commentNumber: "12",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
          date: "January 12, 2019",
        },
        {
          url: require("../assets/images/blog-58 (1).jpg"),
          title: "Top Camper Trailer Towing Tips",
          tags: ['Travel,', 'Lifestyle'],
          author: "John Doe",
          commentNumber: "12",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
          date: "January 12, 2019",
        },
        {
          images: [
            require("../assets/images/blog-13.jpg"),
            require("../assets/images/blog-16.jpg"),
            require("../assets/images/blog-20.jpg"),
            require("../assets/images/blog-23.jpg"),
            require("../assets/images/blog-29.jpg"),
            require("../assets/images/blog-40.jpg")
          ],
          title: "10 Best Travel Tips After 5 Years Traveling The World",
          tags: ['Travel,', 'Lifestyle'],
          author: "John Doe",
          commentNumber: "12",
          content:
            "Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!",
          date: "January 12, 2019",
        },
      ]
    };
  },
};
</script>

<style lang="scss" scoped>

</style>