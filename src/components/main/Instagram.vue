<template>
  <div class="instagram">
    <h4>PHOTOS FROM INSTAGRAM</h4>
    <div class="images">
      <img v-for="(image, index) in images" :key="index" :src="image">
    </div>
    <h4>TAGS</h4>
    <div class="tags">
      <ul>
        <li v-for="tag in tags" :key="tag" class="tag">{{tag}}</li>
      </ul>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Instagram',
    data() {
      return {
        images: [
          require("../../assets/images/29739607_2020680068220520_4509928046932787200_n.jpg"),
          require("../../assets/images/30087804_253872848488989_8792603541668626432_n.jpg"),
          require("../../assets/images/29415620_196477127626244_3250318472361541632_n.jpg"),
          require("../../assets/images/30078414_1274410412703843_8290935809419247616_n.jpg"),
          require("../../assets/images/30077195_2066750973610181_3733150062893596672_n.jpg"),
          require("../../assets/images/29415304_166583630713703_1032667922171953152_n.jpg")
        ],
        tags: ['design', 'brand', 'video', 'business', 'travel']
      }
    }
  }
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  .instagram{
    margin-top: 50px;

    h4{
      font-size: 20px;
      line-height: 20px;
      margin-bottom: 25px;
    }

    .images{
      display: flex;
      flex-wrap: wrap;
      margin-bottom: 30px;

      img{
        width: calc(100% / 3);
      }
    }

    .tags ul{
      display: flex;

      .tag{
        margin-right: 15px;
        padding: 3px 7px;
        font-size: 12px;
        font-weight: 600;
        color: #ffffff;
        background-color: #212529;
        border-radius: 15px;
        text-transform: uppercase;
        cursor: pointer;

        &:last-child{
          margin-right: 0;
        }
      }
    }
  }
  

</style>