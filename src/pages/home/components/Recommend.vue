<template>
  <div>
    <div class="title">
      <img class="img-icon" src="@/assets/images/ebc329f16c55bb02.png" >
      猜你喜欢
      </div>
    <ul>
      <router-link tag="li" :to="'/detail/' + item.id" class="item border-bottom" v-for="item of list" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <div class="mp-like-price">
            <span class="mpg-price">
              ¥<em class="mpg-price-num">{{item.price}}</em>
            </span>起
            </div>
        </div>
      </router-link>
    </ul>
    <a class="mp-like-more mp-border-top" href="//touch.piao.qunar.com/touch/list_广州_景点门票.html">查看所有产品</a>
  </div>
</template>

<script>
import img1 from '@/assets/images/2d7b45e94187416ea3.img.jpg_200x200_7b01f790.jpg'
import img2 from '@/assets/images/ee3013caaa28ae7490.water.jpg_200x200_f052dfc4.jpg'
import img3 from '@/assets/images/898a2df8e97ac037a3.img.jpg_200x200_01aa5ea1.jpg'
import img4 from '@/assets/images/a021cde25761c0aa3.img.jpg_200x200_7635f5ba.jpg'
export default {
  name: 'HomeRecommend',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
 @import '~styles/mixins.styl'
   .mp-like-more
    display: block
    padding: .2rem 0
    color: #00afc7
    font-size: .28rem
    line-height: .4rem
    text-align: center
  .img-icon
    width: .3rem
    height: .3rem
    margin-top: -.1rem
  .title
    margin-top: .2rem
    line-height: .8rem
    text-indent: .2rem
  .item
    overflow: hidden
    display: flex
    height: 1.9rem
    .item-img
      width: 1.7rem
      height: 1.7rem
      padding: .1rem
    .item-info
      flex: 1
      padding: .1rem
      min-width: 0
      .item-title
        line-height: .54rem
        font-size: .32rem
        ellipsis()
      .item-desc
        line-height: .4rem
        color: #ccc
        ellipsis()
      .mp-like-price
        position: relative
        margin-top: .22rem
        color: #616161
        font-size: .24rem
        line-height: .4rem
        .mp-like-price
          color: #ff8300
          font-size: .4rem
        .mpg-price
          color: #ff8300
        .mpg-price-num 
          font-size: .4rem
</style>
