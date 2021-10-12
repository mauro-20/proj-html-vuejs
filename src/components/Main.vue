<template>
  <main>
    <Hero :posts="heroPosts"/>
  </main>
</template>

<script>
import Hero from './main/Hero.vue'

export default {
  name: 'Main',
  components: {
    Hero
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
      ]
    }
  }
}
</script>

<style lang="scss" scoped>

</style>