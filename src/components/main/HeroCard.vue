<template>
  <div class="card">
    <img :src="url">
    <div class="text">
      <div class="tag">{{tag}}</div>
      <div class="title">{{title}}</div>
      <div class="content">{{content}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name:'HeroCard',
  props: {
    url: String,
    tag: String,
    title: String,
    content: String
  }
}
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  .card{
    position: relative;
    height: 250px;
    overflow: hidden;
    background-color: $bg-dark-800;
    
    img{
      width: 100%;
      object-fit: cover;

    }
    .text{
      position: absolute;
      bottom: 0;
      padding: 30px 25px;
      color: $text-light-100;
      cursor: context-menu;

      .tag{
        display: inline-block;
        margin-bottom: 12px;
        padding: 5px;
        border-radius: 2px;
        background-color: $bg-primary;
        font-size: 8px;
        font-weight: 600;
        text-transform: uppercase;
      }
      .title{
        text-transform: capitalize;
        font-size: 1.2rem;
        font-weight: 700;
        line-height: 1.5625rem;
      }
      .content{
        display: none;
        font-size: 12px;
        font-weight: 800;
        color: $text-light-300;
        line-height: 1.5rem;
      }
    }

    &:hover img{
      opacity: 0.2;
    }
    &:hover .content{
      display: block;
    }
  }

</style>