<template>
  <main>
    <Hero :posts="heroPosts"/>
    <TopPosts :popular="popularPosts" :recent="recentPosts"/>
  </main>
</template>

<script>
import Hero from './main/Hero.vue'
import TopPosts from './main/TopPosts.vue'

export default {
  name: 'Main',
  components: {
    Hero,
    TopPosts
  },
  data() {
    return {
      heroPosts: [
        {
          url: require('../assets/images/blog-46.jpg'),
          title: 'how to take better concert picture in 30 seconds',
          tag: 'photography',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!'
        },
        {
          url: require('../assets/images/blog-47.jpg'),
          title: 'gadgets that make your smartphone even smarter',
          tag: 'gadgets',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!'
        },
        {
          url: require('../assets/images/blog-48.jpg'),
          title: '20 top-rated tourist attractions in manhattan',
          tag: 'travel',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!'
        },
        {
          url: require('../assets/images/blog-49.jpg'),
          title: 'the best way to ride a motorcycle',
          tag: 'lifstyle',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!'
        },
        {
          url: require('../assets/images/blog-50.jpg'),
          title: '5 fun things to do at the beach',
          tag: 'travel',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!'
        },
        {
          url: require('../assets/images/blog-51.jpg'),
          title: 'amazingly fresh fruit and herbs drinks for summer',
          tag: 'recipes',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!'
        }
      ],
      popularPosts: [
        {
          url: require('../assets/images/blog-55.jpg'),
          title: 'Simple Ways to Have a Pretty Face',
          tag: 'lifestyle',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!',
          date: 'January 12, 2019'
        },
        {
          url: require('../assets/images/blog-56.jpg'),
          title: 'Ranking the greatest players in basketball',
          tag: 'sport',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!',
          date: 'January 12, 2019'
        },
        {
          url: require('../assets/images/blog-57.jpg'),
          title: '4 Ways to Look Cool in Glasses',
          tag: 'photography',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!',
          date: 'January 12, 2019'
        },
        {
          url: require('../assets/images/blog-58.jpg'),
          title: 'Top Camper Trailer Towing Tips',
          tag: 'travel',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!',
          date: 'January 12, 2019'
        },
        {
          url: require('../assets/images/blog-59.jpg'),
          title: '5 Lovely Walks in New York',
          tag: 'travel',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!',
          date: 'January 12, 2019'
        }
      ],
      recentPosts: [
        {
          url: require('../assets/images/blog-65.jpg'),
          title: 'Main Reasons To Stop Texting And Driving',
          tag: 'lifestyle',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!',
          date: 'January 12, 2019'
        },
        {
          url: require('../assets/images/blog-66.jpg'),
          title: 'Tips to Help You Quickly Prepare your Lunch',
          tag: 'recipe',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!',
          date: 'January 12, 2019'
        },
        {
          url: require('../assets/images/blog-67.jpg'),
          title: 'Why should I buy a smartwatch',
          tag: 'tech',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!',
          date: 'January 12, 2019'
        },
        {
          url: require('../assets/images/blog-68.jpg'),
          title: 'The best augmented reality smartglasses',
          tag: 'tech',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!',
          date: 'January 12, 2019'
        },
        {
          url: require('../assets/images/blog-69.jpg'),
          title: '12 Helthiest Foods to Eat for Breakfast',
          tag: 'recipe',
          content: 'Quisquam numquam aspernatur accusantium iusto blanditiis quis pariatur fugiat, eius vero perferendis!',
          date: 'January 12, 2019'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

</style>