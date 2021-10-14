<template>
  <div class="tag">
    {{category}}
  </div>
</template>

<script>
  export default {
    name: 'Category',
    props: {
      category: String
    }
  }
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  .tag{
    display: inline-block;
    margin: 0 7px 9px 0;
    padding: 8px;
    border-radius: 3px;
    font-size: 12px;
    font-weight: 700;
    text-transform: uppercase;
    color: $text-light-100;
    background-color: $bg-dark-900;
    cursor: pointer;
  }

</style>