<template lang="html">
<div>
  <div class="index-top-bg" :class="{'swiper-top': banner && banner.length > 0}">
    <div class="top-title">购物先省钱</div>
    <div class="search-wrap">
      <i class="search-icon"></i>
      <input class="search-input" placeholder="复制淘宝商品标题搜索优惠券" type="text" />
      <a class="search-btn" href="#">搜索</a>
    </div>
    <div class="top-txt">
      <p><i>1</i>复制淘宝商品标题</p>
      <p class="center-line"></p>
      <p><i>2</i>打开购省钱搜券</p>
    </div>
  </div>

  <!-- 轮播图1 -->
  <div class="slide" id="swiper1">
    <div>
      <template v-for="item1 in banner">
        <p @click="gotoSearch(item1.action_id)"><img :src="item1.picUrl" alt=""></p>
      </template>
    </div>
  </div>

  <!-- 分类专题 -->
  <ul class="module-type">
    <li>
      <img src="./assets/img/icon_search.png">
      <span>今日必买</span>
    </li>
    <li>
      <img src="./assets/img/icon_search.png">
      <span>今日必买</span>
    </li>
    <li>
      <img src="./assets/img/icon_search.png">
      <span>今日必买</span>
    </li>
    <li>
      <img src="./assets/img/icon_search.png">
      <span>今日必买</span>
    </li>
    <li>
      <img src="./assets/img/icon_search.png">
      <span>今日必买</span>
    </li>
  </ul>

  <!-- 轮播图2 -->
  <div class="slide" id="swiper2">
    <div>
      <template v-for="item1 in banner">
        <img :src="item1.picUrl" alt="">
      </template>
    </div>
  </div>

  <!-- 商品专题 -->
  <div class="module-goods">
    <ul class="goods sort5">
      <li><img src="./assets/img/top-banner.png"></li>
      <li><img src="./assets/img/top-banner.png"></li>
      <li><img src="./assets/img/top-banner.png"></li>
      <li><img src="./assets/img/top-banner.png"></li>
      <li><img src="./assets/img/top-banner.png"></li>
      <li><img src="./assets/img/top-banner.png"></li>
      <li><img src="./assets/img/top-banner.png"></li>
    </ul>
  </div>

  <!-- 商品详情 -->
  <div class="goods-wrap">
    <ul class="goods-tab">
      <li><a href="javascript:;">精选</a></li>
      <li><a href="javascript:;">精选</a></li>
      <li><a href="javascript:;">精选</a></li>
      <li><a href="javascript:;">精选</a></li>
      <li><a href="javascript:;">精选</a></li>
      <li class="active"><a href="javascript:;">精选</a> </li>
    </ul>
    <ul class="goods-list">
      <li>
        <img class="img" src="./assets/img/top-banner.png" alt="">
        <div class="goods-info">
          <p class='goods-name'>
            <i class="icon-tao"></i>
            <!-- <i class="icon-tmall"></i> -->充氮酱板鸭62g湖南特产舜华临武鸭保险包装产舜华临武鸭保险包装
          </p>
          <div class="goods-price">
            <p class='price'>券后<span>￥<i>68.0</i></span></p>
            <!-- <p class="price-old"><span v-html="item.goodsType ===0 ? '淘宝价' : '天猫价'"></span><s>¥{{ item.costPrice }}</s></p> -->
            <p class="price-old"><span>淘宝价</span><s>¥118</s></p>
            <p class='coupon'>券¥50</p>
            <p class="num">4520人领券</p>
          </div>
        </div>
      </li>
      <li>
        <img class="img" src="./assets/img/top-banner.png" alt="">
        <div class="goods-info">
          <p class='goods-name'>
            <i class="icon-tao"></i>
            <!-- <i class="icon-tmall"></i> -->充氮酱板鸭62g湖南特产舜华临武鸭保险包装产舜华临武鸭保险包装
          </p>
          <div class="goods-price">
            <p class='price'>券后<span>￥<i>68.0</i></span></p>
            <!-- <p class="price-old"><span v-html="item.goodsType === 0 ? '淘宝价' : '天猫价'"></span><s>¥{{ item.costPrice }}</s></p> -->
            <p class="price-old"><span>淘宝价</span><s>¥118</s></p>
            <p class='coupon'>券¥50</p>
            <p class="num">4520人领券</p>
          </div>
        </div>
      </li>
      <li>
        <img class="img" src="./assets/img/top-banner.png" alt="">
        <div class="goods-info">
          <p class='goods-name'>
            <i class="icon-tao"></i>
            <!-- <i class="icon-tmall"></i> -->充氮酱板鸭62g湖南特产舜华临武鸭保险包装产舜华临武鸭保险包装
          </p>
          <div class="goods-price">
            <p class='price'>券后<span>￥<i>68.0</i></span></p>
            <!-- <p class="price-old"><span v-html="item.goodsType === 0 ? '淘宝价' : '天猫价'"></span><s>¥{{ item.costPrice }}</s></p> -->
            <p class="price-old"><span>淘宝价</span><s>¥118</s></p>
            <p class='coupon'>券¥50</p>
            <p class="num">4520人领券</p>
          </div>
        </div>
      </li>
      <li>
        <img class="img" src="./assets/img/top-banner.png" alt="">
        <div class="goods-info">
          <p class='goods-name'>
            <i class="icon-tao"></i>
            <!-- <i class="icon-tmall"></i> -->充氮酱板鸭62g湖南特产舜华临武鸭保险包装产舜华临武鸭保险包装
          </p>
          <div class="goods-price">
            <p class='price'>券后<span>￥<i>68.0</i></span></p>
            <!-- <p class="price-old"><span v-html="item.goodsType === 0 ? '淘宝价' : '天猫价'"></span><s>¥{{ item.costPrice }}</s></p> -->
            <p class="price-old"><span>淘宝价</span><s>¥118</s></p>
            <p class='coupon'>券¥50</p>
            <p class="num">4520人领券</p>
          </div>
        </div>
      </li>
      <li>
        <img class="img" src="./assets/img/top-banner.png" alt="">
        <div class="goods-info">
          <p class='goods-name'>
            <i class="icon-tao"></i>
            <!-- <i class="icon-tmall"></i> -->充氮酱板鸭62g湖南特产舜华临武鸭保险包装产舜华临武鸭保险包装
          </p>
          <div class="goods-price">
            <p class='price'>券后<span>￥<i>68.0</i></span></p>
            <!-- <p class="price-old"><span v-html="item.goodsType === 0 ? '淘宝价' : '天猫价'"></span><s>¥{{ item.costPrice }}</s></p> -->
            <p class="price-old"><span>淘宝价</span><s>¥118</s></p>
            <p class='coupon'>券¥50</p>
            <p class="num">4520人领券</p>
          </div>
        </div>
      </li>
    </ul>
  </div>
</div>
</template>

<script>
import { bangClick } from '../../common/config.js'
import { RoomSlider } from '../../common/slider.js'
import { mapState, mapActions, mapGetters, mapMutations } from 'vuex'
export default {
  data () {
    return{
      banner: [], //顶部轮播banner
      focusBanner: [], //焦点banner
      actBanner: [],  //中部轮播banner
      specialBanner: [], //专题banner
    }
  },
  computed: {
  },
  created () {
    this.getBanner();
  },
  methods: {
    ...mapActions(['fetchPcApiBanner']),
    getBanner() {
      this.fetchPcApiBanner({params: {}, cb: (err, data) => {
        console.log(data)
        if(data && data.code === 200) {
          this.banner = data.data.banner;
          this.focusBanner = data.data.focusBanner;
          this.actBanner = data.data.actBanner;
          this.specialBanner = data.data.specialBanner;
          this.$nextTick(function () {
            let slider1 = new RoomSlider('swiper1');
            let slider2 = new RoomSlider('swiper2');
          })
        } else {
          this.$toast(data && data.msg || '网络错误')
        }
      }})
    },
    gotoSearch(actionId) {
      console.log(actionId);
      // location.href = "http://www.goushengqian.com/search.html?type=" + actionId;
    }
  }
}
</script>

<style lang="scss">
  @import '../../assets/mixin';
  .index-top-bg{
    width: 640px;
    height: 218px;
    background: no-repeat center/cover linear-gradient(90deg, #ff5028, #ff1c34);
    &.swiper-top{
      height: 310px;
    }
    .top-title{
      height: 82px;
      line-height: 82px;
      text-align: center;
      color: #fff;
      font-size: 32px;
    }
    .search-wrap{
      display: flex;
      width: 600px;
      height: 68px;
      margin: 0 auto;
      position: relative;
      .search-icon{
          width: 23px;
          height: 23px;
          background: url(./assets/img/icon_search.png) no-repeat center/cover;
          position: absolute;
          top: 22px;
          left: 30px;
      }
      .search-input{
        width: 424px;
        height: 68px;
        background: #fff;
        color: #333;
        border-radius: 68px 0 0 68px;
        border: 0 none;
        font-size: 24px;
        padding: 0 60px;
        &::-webkit-input-placeholder{
          font-size: 24px;
          color: #666666;
        }
      }
      .search-btn{
        display: block;
        width: 116px;
        height: 68px;
        line-height: 68px;
        font-size: 28px;
        color: #7e2d00;
        background: #ffd435;
        text-align: center;
        border-radius: 0 68px 68px 0;
      }
    }
    .top-txt{
      display: flex;
      margin: 0 40px;
      height: 60px;
      line-height: 60px;
      p{
        font-size: 24px;
        color: #fff;
        i{
          width: 24px;
          height: 24px;
          display: inline-block;
          border:1PX solid #fff;
          border-radius: 24px;
          text-align: center;
          line-height: 24px;
          font-size: 16px;
          margin-right: 10px;
        }
      }
      .center-line{
        display: inline-block;
        width: 60px;
        height: 2px;
        background: rgba(255,255,255,.5);
        margin: 32px 20px;
      }
    }
  }

  // 轮播1
  .swiper-wrap{
    background: blue;
    width: 600px;
    height: 196px;
    margin: -100px auto 0;
    position: relative;
    overflow: hidden;
    .slider{
      width: 100%;
      height: 100%;
      .img{
        width: 100%;
        height: 100%;
        display: block;
      }
    }
    &.swiper-wrap2{
      margin-top: 0;
    }
    .swiper-wrapper{
      img{
        display: block;
        width: 600px;
        height: 196px;
      }
    }
    .swiper-button-prev, .swiper-button-next{
      width: 40px;
      height: 40px;
      margin-top: -20px;
    }
    .swiper-button-next, .swiper-container-rtl .swiper-button-prev{
      background: url(./assets/img/right.png) no-repeat center/cover;
      right: 0;
    }
    .swiper-button-prev, .swiper-container-rtl .swiper-button-next{
      background: url(./assets/img/left.png) no-repeat center/cover;
      left: 0;
    }
    .swiper-pagination{
      position: absolute;
      bottom: 8px;
      left: 50%;
      transform: translateX(-50%);
      padding: 4px 12px;
      height: 8px;
      margin: 0 auto;
      background: rgba(255,255,255,.34);
      border-radius: 8px;
    }
    .my-bullet{
      display: inline-block;
      width: 8px;
      height: 8px;
      background: #fff;
      opacity: 1;
      border-radius: 8px;
      margin-right: 8px;
      position: relative;
      top: -20px;
      &:last-child{
        margin-right: 0;
      }
    }
    .my-bullet-active{
      width: 20px;
      height: 8px;
      background: #ff341f;
    }
  }

  // 配置模块
  .module-type{
    padding: 25px 16px 0;
    overflow: hidden;
    background: #ccc;
    li{
      float: left;
      width: 20%;
      text-align: center;
      margin-bottom: 30px;
      img{
        display: block;
        width: 80px;
        height: 80px;
        margin: 0 auto;
      }
      span{
        font-size: 24px;
        color: #333333;

      }
    }
  }

  // 配置商品
  .module-goods{
    margin: 30px 18px 0;
    .goods{
      overflow: hidden;
      li{
        float: left;
        margin:0 0 8px 8px;
        width: 296px;
        height: 146px;
        img{
          width: 100%;
          height: 100%;
        }
        &:first-child{
          margin-left: 0;
          width: 296px;
          height: 300px;
          img{
            width: 100%;
            height: 100%;
          }
        }
      }
    }
    .sort5{
      li:nth-child(4),li:nth-child(6){
        width: 296px;
        height: 146px;
        float: left;
        margin: 0 8px 8px 0;
      }
      li:nth-child(5), li:nth-child(7){
        width: 296px;
        height: 146px;
        float: left;
        margin: 0 0 8px 0;
      }
    }
  }

  // 商品详情
  .goods-wrap{
    margin: 10px 18px 0;
    .goods-tab{
      display: flex;
      li{
        flex:1;
        font-size: 28px;
        text-align: center;
        a{
          color: #222222;
          padding-bottom: 10px;
        }
        &::after{
          content: '';
          // width: 2px;
          height: 24px;
          border-left: 2px solid #e5e5e5;
          background: #e5e5e5;
          display: inline-block;
          margin: 8px 0 0 20px;
        }
        &:last-child{
          &::after{
            border-left: 0 none;
          }
        }
        &.active{
          a{
            color: #ff2235;
            border-bottom: 4px solid #ff3c31;
          }
        }
      }
    }
  }
  // 商品列表
  .goods-list{
    padding-top: 30px;
    li{
      display: flex;
      padding-bottom: 36px;
    }
    .img{
      width: 204px;
      height: 204px;
      border-radius: 20px;
    }
    .goods-info{
      flex:1;
      width: 350px;
      padding: 0 0 0 20px;
      overflow: hidden;
      position: relative;
      .goods-name{
        color:#222222;
        font-size: 28px;
        line-height: 40px;
        height: 80px;
        display:-webkit-box;
        -webkit-line-clamp: 2;
        -webkit-box-orient:vertical;
        text-overflow: ellipsis;
        overflow: hidden;
        margin-bottom:12px;
        padding:8px 0 0;
      }
      .icon-tao{
        display: inline-block;
        width: 28px;
        height: 28px;
        background:url(./assets/img/icon_tao.png) center/100% no-repeat;
        vertical-align: middle;
      }
      .icon-tmall{
        @extend .icon-tao;
        background:url(./assets/img/icon_tmall.png) center/100% no-repeat;
      }
      >.goods-discount{
        padding-bottom: 20px;
        padding-top: 5px;
        .left-icon{
          flex:1;
          display: inline-block;
          border: 1PX solid #d6d6d6;
          height: 34px;
          font-size: 22px;
          line-height: 36px;
          color: #999999;
          border-radius: 36px;
          padding: 0 15px;
          vertical-align: middle;
        }
        .right-icon{
          @extend .left-icon;
          color: #ff5933;
          border: 1PX solid #ffbdad;
        }
      }
      .goods-price{
        position: absolute;
        bottom: 12px;
        left: 20px;
        width: 380px;
        .price-old{
          font-size: 24px;
          color: #999;
          padding-top: 5px;
        }
        .price{
          color:#fe0000;
          font-size: 28px;
          line-height: 50px;
          >span{
            color: #fe0000;
            i{
              font-size: 40px;
              font-weight: bold;
            }
          }
        }
        .coupon{
          display:inline-block;
          width: 114px;
          height: 40px;
          line-height: 42px;
          background:url(./assets/img/coupon.png) center/contain no-repeat;
          font-size: 28px;
          color: #fff;
          text-align: center;
          position: absolute;
          vertical-align: middle;
          right: 0;
          top: 8px;
        }
        .num{
          font-size: 24px;
          color: #999;
          position: absolute;
          right: 15px;
          top: 60px;
        }
      }
    }
  }
  

  // js轮播 样式
  .slide{
    // background: blue;
    width: 600px;
    height: 196px;
    margin: -80px auto 0;
    position: relative;
    overflow: hidden;
    .room{
      width: 100%;
      height: 100%;
      img{
        width: 598px;
        height: 196px;
        display: block;
        float: left;
        border: 0 none;
        margin: 0 auto;
      }
    }
  }
  
</style>
