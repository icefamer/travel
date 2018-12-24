<template>
  <div>
    <div class="title">热销推荐</div>
    <ul>
      <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
        <img class="item-img" :src="item.imgUrl">
        <div class="item-info">
          <p class="item-title">{{item.title}}</p>
          <p class="item-desc">{{item.desc}}</p>
          <p class="item-price">{{item.price}}</p>
          <button class="item-button">查看详情</button>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data () {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1411/43/dea8b51719a4a69b68777baa68c146e4.water.jpg_200x200_8da8cebe.jpg',
        title: '春晖园温泉度假村',
        desc: '享受冬日温情',
        price: '199.0'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1712/71/71ace1aa7d971212a3.water.jpg_200x200_9638020d.jpg',
        title: '渔阳滑雪场',
        desc: '让冬天的温度high起来',
        price: '119.0'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1411/43/dea8b51719a4a69b68777baa68c146e4.water.jpg_200x200_8da8cebe.jpg',
        title: '春晖园温泉度假村',
        desc: '享受冬日温情',
        price: '199.0'
      }, {
        id: '0004',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1712/71/71ace1aa7d971212a3.water.jpg_200x200_9638020d.jpg',
        title: '渔阳滑雪场',
        desc: '让冬天的温度high起来',
        price: '119.0'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import '~styles/mixins.styl';
  .title
    margin-top .2rem
    line-height .8rem
    background-color #eeeeee
    text-indent .2rem
  .item
    display flex
    height 1.9rem
    overflow hidden
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      flex 1
      padding .1rem
      min-width 0
      .item-title
        line-height .45rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #cccccc
        ellipsis()
      .item-price
        line-height .45rem
        font-size .35rem
      .item-button
        line-height .44rem
        background-color #ff9300
        padding 0 .2rem
        border-radius .06rem
        color #ffffff
</style>
