<template>
  <div class="author-thumb">
    <img :src="details.url">
    <div class="thumb-text">  
      <div class="thumb-title">{{details.name}}</div>
      <div class="info">{{details.info}}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'AuthorThumb',
  props: {
    details: Object
  }
}
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  .author-thumb{
    display: flex;
    align-items: center;
    padding: 15px 0;
       
    img{
      width: 120px;
      margin-right: 20px;
    }
    .thumb-title{
      font-size: 16px;
      font-weight: 600;
      margin-bottom: 6px;
    }
    .info{
      font-size: 14px;
      font-weight: 500;
      color: $text-light-200;
    }

  }

</style>