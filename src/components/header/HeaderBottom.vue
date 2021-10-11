<template>
  <div class="header-bottom">
    <div class="container">
      <div class="logo">
        <img :src="logoUrl" alt="logo">
      </div>
    </div>
    <div class="main-nav">
      <div class="container">
        <ul>
          <li v-for="menu in nav" :key="menu"><a href="#">{{menu}}</a></li>
        </ul>
        <div class="search">
          <button class="btn-search">
            <i class="fas fa-search"></i>
          </button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeaderBottom',
  props: {
    logoUrl: String,
    nav: Array
  }
}
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';
  
  .header-bottom{
    background-color: $bg-light-100;

    .logo{
      width: 130px;
      padding: 35px 0;

      img{
        width: 100%;
      }
    }
    .main-nav{
      border-top: 1px solid $bd-light-400;

      .container{
        display: flex;
        justify-content: space-between;
        align-items: center;
      
        ul{
          display: flex;
          padding: 20px 0;

          li{
            margin-right: 3.5rem;

            a{
              font-weight: 600;
              text-transform: uppercase;
            }
            &:hover{
              color: $text-primary;
            }
          }
        }
        .btn-search{
          border: none;
          background-color: transparent;
          cursor: pointer;
        }
      }
    }
  }

  



</style>