<template>
  <div class="facebook">
    <h4>FIND US ON FACEBOOK</h4>
    <div class="theme">Okler Themes</div>
  </div>
</template>

<script>
export default {
  name: 'Facebook'
}
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  h4{
    font-size: 20px;
    line-height: 20px;
    margin-bottom: 25px;
  }
  .theme{
    height: 40px;
    line-height: 40px;
    padding-left: 15px;
    border-left: 5px solid $bd-light-300;
    color: $text-primary;
    font-weight: 600;
    cursor: pointer;
  }

</style>