<template>
  <div class="header-top">
    <div class="container">
      <ul>
        <li>Everything about Lifestyle, Travel and Gadgets!</li>
        <li><a href="#">sign in</a></li>
        <li><a href="#">about us</a></li>
        <li><a href="#">contact us</a></li>
        <li><a href="#">buy now</a></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderTop'
}
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  .header-top{
    padding: 1.5625rem 0;
    font-size: .875rem;
    background-color: $bg-primary;
    color: $text-light-100;

    ul{
      display: flex;

      li{
        margin-right: 1.5625rem;

        a{
          text-transform: uppercase;
        }
      }
    }
  }

</style>