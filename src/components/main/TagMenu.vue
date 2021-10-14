<template>
  <section>
    <nav class="container">
      <button class="btn-nav"><i class="fas fa-angle-left"></i></button>
      <ul>
        <li v-for="tag in tags" :key="tag">
          <a href="#">{{tag}}</a>
        </li>
      </ul>
      <button class="btn-nav"><i class="fas fa-angle-right"></i></button>
    </nav>
  </section>
</template>

<script>
export default {
  name: 'TagMenu',
  props: {
    tags: Array
  }
}
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  section{
    padding: 50px 0;
    background-color: $bg-primary;

    .container{
      display: flex;
      justify-content: space-between;
      align-items: center;

      .btn-nav{
        padding: 10px;
        font-size: 20px;
        color: $bg-opacity-200;
        background-color: transparent;
        border: none;
        cursor: pointer;
      }

      ul{
        display: flex;
        justify-content: center;
        li{
          margin: 0 12px;
        }
        a{
          display: inline-block;
          width: 185px;
          height: 50px;
          font-weight: 700;
          text-align: center;
          line-height: 50px;
          text-transform: uppercase;
          color: $text-light-100;
          background-color: $bg-dark-700;
        }
      }
    }
    
  }


</style>