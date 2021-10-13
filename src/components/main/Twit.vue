<template>
  <div class="twit">
    <div class="logo">
      <i class="fab fa-twitter"></i>
    </div>
    <div class="content">
      <div class="text">{{details.content}}</div>
      <div class="date">{{details.date}}</div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Twit',
    props: {
      details: Object
    }
  }
</script>

<style lang="scss" scoped>  
  @import '../../assets/style/variables';

  .twit{
    display: flex;
    margin-bottom: 30px;

    .logo{
      margin-right: 10px;
    }
    .text{
      color: $text-light-300;
      margin-bottom: 10px;
    }
    .date{
      color: $text-primary;
    }
  }

</style>