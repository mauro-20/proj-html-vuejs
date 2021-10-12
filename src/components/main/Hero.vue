<template>
  <section class="hero">
    <div class="container">
      <ul>
        <li v-for="(post, index) in posts" :key="index">
          <HeroCard :post="post"/>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
import HeroCard from "./HeroCard.vue";

export default {
  name: "Hero",
  components: {
    HeroCard,
  },
  props: {
    posts: Array
  }
};
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  .hero{
    background-color: $bg-light-200;
    padding: 30px 0;

    ul{
      display: flex;
      flex-wrap: wrap;
      
      li{
        width: calc((100% - 30px) / 3);
        margin-right: 15px;
        margin-bottom: 15px;
        
        &:nth-child(3n){
          margin-right: 0;
        }
      }
    }
  }

</style>