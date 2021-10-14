<template>
  <div class="post">
    <img :src="post.url">
    <div class="content">
      <div class="text">{{post.content}}</div>
      <div class="date">{{post.date}}</div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Post',
    props: {
      post: Object
    }
  }
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  .post{
    display: flex;
    margin-bottom: 20px;
    cursor: pointer;
    img{
      width: 80px;
      height: 80px;
      margin-right: 20px;
      border-radius: 50%;
    }
    .text{
      margin-bottom: 10px;
      font-size: 14px;
      color: $text-light-200;
    }
    .date{
      font-size: 12px;
      color: $text-dark-500;
    }
  }

</style>