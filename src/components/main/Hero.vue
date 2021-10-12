<template>
  <section class="hero">
    <div class="container">
      <HeroCard />
      <HeroCard />
      <HeroCard />
      <HeroCard />
      <HeroCard />
      <HeroCard />
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
};
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  .hero{
    background-color: $bg-light-200;

    .container {
      display: flex;
      flex-wrap: wrap;

      *{
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