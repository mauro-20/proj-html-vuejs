<template>
  <div class="small-thumb">
    <h3 class="title">popular posts</h3>
    <ul>
      <li v-for="(post, index) in posts" :key="index" class="post">
        <img :src="post.url">
        <div class="post-text">  
          <div class="post-title">{{post.title}}</div>
          <div class="date">{{post.date}}</div>
        </div>
      </li>
    </ul>
    
  </div>
</template>

<script>
export default {
  name: 'SmallThumb',
  props: {
    title: String,
    posts: Array
  }
}
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  .title{
    text-transform: uppercase;
    margin-bottom: 5px;
  }

  .post{
    display: flex;
    padding: 15px 0;
    border-bottom: 1px dotted $text-light-200;

    &:last-child{
      border: none;
    }
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