<template>
  <div class="home">
    <top-nav></top-nav>
    <div class="content">
      <div class="img">
        <img src="../assets/logo1.png" alt="" srcset="">
      </div>
      <div class="text">
        <h1>WeUI Design</h1>
        <H4>面向学习开发的开源框架用于开拓眼界</H4>
        <div class="btn">
          <a target="_blank" href="https://qqiang-g.github.io/weui/" class="git">GitHub</a>
          <router-link to="/doc">开始</router-link>
        </div>
      </div>
    </div>
    <div class="desc">
      <div class="item">
        <div>
          <div class="title">基于Vue3</div>
          <div class="d-x">使用了Vue3 Composition API</div>
        </div>
      </div>
      <div class="item">
        <svg class="icon" aria-hidden="true">
          <use xlink:href="#g-typescript"></use>
        </svg>
        <div>
          <div class="title">基于Typescript</div>
          <div class="d-x">源代码采用Typescript书写（非常严格）</div>
        </div>
      </div>
      <div class="item">
        <svg class="icon" aria-hidden="true">
          <use xlink:href="#g-weibiaoti-"></use>
        </svg>
        <div>
          <div class="title">代码易读</div>
          <div class="d-x">每个组件的源代码都极其简洁</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TopNav from '../components/Topnav.vue'
export default {
  name:'home',
  components: {TopNav},
}
</script>

<style lang="scss" scoped>
$h1_color: #12b9b9;
$bg:#12b9b9;
$btn_color: #fff;
$border_radius: 4px;
.home {
  ::v-deep(.top-nav) {
    background: transparent;
  }

  .content {
    background: linear-gradient(145deg, #c1e6e683 0%, #88dada83 100%);
    margin: 0 auto;
    clip-path: ellipse(80% 60% at 50% 40%);
    padding: 100px 0 150px 0;
    display: flex;
    flex-wrap: wrap;
    >.img{
      width: 100vw;
      text-align: center;
    }
    >.text{
      width: 100vw;
      text-align: center;
    }

    > h1 {
      text-align: center;
      font-size: 34px;
      line-height: 52px;
      color: $h1_color;
    }
    >h2 {
      text-align: right;
      padding-right: 100px;
      font-size: 20px;
      line-height: 26px;
      color: $h1_color;
      margin-top: 12px;
    }
    .btn{
      text-align: center;
      margin-top: 16px;
      font-size: 17px;
      .git{
        margin-right: 15px;
      }
      >a {
        background: $bg;
        padding: 8px 20px;
        color: $btn_color;
        border-radius: $border_radius;
      }
    }
  }
  .desc{
    display: flex;
    padding-top: 70px;
    .item{
      flex: 1;
      display: flex;
      justify-content: center;
      >svg{
        width: 45px;
        height: 45px;
        margin-right: 15px;
      }
      .title{
        font-size: 28px;
        margin-bottom: 12px;
      }
      .d-x{
        font-size: 20px;
      }
    }
  }
}
@media screen and (max-width: 900px){
  .home{
    .content{
      padding: 100px 0 50px 0;
      >h2{
        padding-right: 0;
        text-align: center;
        margin-bottom: 15px;
      }
      .btn{
        display: block;
        text-align: center;
        margin: 0 auto;
        width: 300px;
        padding: 0 40px 30px;
        .git{
          margin-right: 0;
          margin-bottom: 15px;
        }
        >a{
          display: inline-block;
          min-width: 8em;
        }
      }
    }
    .desc{
      padding-bottom: 200px;
      flex-direction: column;
      .item{
        display: block;
        text-align: center;
        margin: 0 auto;
        width: 300px;
        padding: 0 40px 30px;
        .title{
          font-size: 20px;
        }
        .d-x{
          font-size: 14px;
          line-height: 20px;
        }
        >svg{
          margin-bottom: 10px;
          margin-right: 0;
        }
      }
    }
  }
}
</style>
