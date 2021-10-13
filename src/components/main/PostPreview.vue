<template>
  <div class="post">
    <div class="poster">
      <img v-if="post.url" :src="post.url" class="single-img" >
      <div v-if="post.images" class="mosaic">
        <img v-for="(url, index) in post.images" :key="index" :src="url">
      </div>
    </div>
    <div class="post-bottom">
      <div class="date">
        <div class="day">12</div>
        <div class="month">JAN</div>
      </div>
      <div class="content">
        <h3 class="title">{{post.title}}</h3>
        <div class="text">{{post.content}}}</div>
        <div class="details">
          <div class="tags">
            <span class="tag">
              <i class="far fa-user"></i> By<span class="primary"> {{post.author}}</span> 
            </span>
            <span class="tag">
              <i class="far fa-folder"></i>
              <span class="primary" v-for="(tag, index) in post.tags" :key="index"> {{tag}}</span>
            </span>
            <span class="tag">
              <i class="far fa-comments"></i><span class="primary"> {{post.commentNumber}} Comments</span>
            </span>
          </div>
          <button class="btn-more">READ MORE</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PostPreview',
  props: {
    post: Object
  }
}
</script>

<style lang="scss" scoped>
  @import '../../assets/style/variables';

  .post{
    margin-bottom: 50px;
    .poster{
      margin-bottom: 25px;
      .single-img{
        width: 100%;
      }
      .mosaic{
        display: flex;
        flex-wrap: wrap;
        img{
          width: calc(100% / 3);
        }
      }
    }
    .post-bottom{
      display: flex;
    
      .date{
        display: inline-block;
        margin-right: 25px;
        font-weight: 600;
        .day{
          color: $text-dark-800;
          background-color: $bg-light-200;
          height: 50px;
          width: 40px;
          line-height: 50px;
          text-align: center;
        }
        .month{
          color: $bg-light-200;
          background-color: $bg-dark-800;
          height: 20px;
          width: 40px;
          line-height: 20px;
          text-align: center;
          font-size: 10px;
        }
      }
      .content{
        .title{
          margin-bottom: 25px;
          font-size: 25px;
          line-height: 25px;
          font-weight: 600;
        }
        .text{
          margin-bottom: 25px;
          color: $text-light-300;
          line-height: 1.5rem;
        }
        .details{
          display: flex;
          justify-content: space-between;
          align-items: center;
          padding-bottom: 25px;
          border-bottom: 1px solid $bd-light-600;

          .tags{
            font-size: 14px;
            color: $text-light-300;
            .tag{
              margin-right: 15px;
            }
            .primary{
              color: $text-primary;
              cursor: pointer;
            }
          }
        }
        .btn-more{
          margin-right: 10px;
          padding: 5px 8px;
          font-weight: 500;
          color: $text-light-400;
          background-color: transparent;
          border: 1px solid $text-light-400;
          border-radius: 5px;
          cursor: pointer;
        }
      }

    }
  }

</style>