<template>
  <div class="comment">
    <div class="text">
      <span class="primary">> </span>
      <span class="user">{{comment.user}}</span>
      commented on
      <span class="primary">{{comment.post}}</span>
    </div>
    <div class="date">{{comment.date}}</div>
  </div>
</template>

<script>
  export default {
    name: 'Comment',
    props: {
      comment: Object
    }
  }
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  .comment{
    line-height: 28px;
    font-size: 14px;
    margin-bottom: 15px;
    .text{
      margin-bottom: 7px;
      color: $text-light-200;
    }
    .primary{
      color: $text-primary;
      cursor: pointer;
    }
    .user{
      color: $text-light-100;
      font-weight: 600;
      cursor: pointer;
    }
    .date{
      color: $text-dark-500;
    }
  }
  
  

</style>