<template>
  <div class="small-thumb">
    <img :src="post.url">
    <div class="post-text">  
      <div class="post-title">{{post.title}}</div>
      <div class="date">{{post.date}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SmallThumb',
  props: {
    post: Object
  }
}
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  .small-thumb{
    display: flex;
    padding: 15px 0;
    cursor: pointer;
       
    img{
      width: 70px;
      margin-right: 15px;
    }
    .post-title{
      font-size: 16px;
      margin-bottom: 4px;
    }
    .date{
      font-size: 14px;
      font-weight: 500;
      color: $text-light-300;
    }

  }

</style>