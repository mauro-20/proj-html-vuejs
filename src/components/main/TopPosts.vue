<template>
  <section class="top-posts">
    <div class="container">
      <div class="col">
        <SmallThumb title="popular posts" :posts="popular"/>
      </div>
      <div class="col">
        <SmallThumb title="recent posts" :posts="recent"/>
      </div>
      <div class="col">

      </div>
    </div>
  </section>
</template>

<script>
  import SmallThumb from './SmallThumb.vue'

  export default {
    name: 'TopPosts',
    components: {
      SmallThumb
    },
    props: {
      popular: Array,
      recent: Array
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
      }
    }
  }

</style>