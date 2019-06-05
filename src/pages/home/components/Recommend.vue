<template>
    <div>
      <div class='title'>热销推荐 </div>
      <ul>
        <li class='item border-bottom' v-for="item of recommendList" :key="item.id">
          <img class='item-img' :src="item.imgUrl">
          <div class='item-info'>
            <p class='item-title'>{{item.title}}</p>
            <p class='item-desc'>{{item.desc}}</p>
            <button class='item-button'>查看详情</button>
          </div>
        </li>
      </ul>
    </div>
</template>

<script>
export default {
  name: 'HomeRecommend',
  data() {
    return {
      recommendList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1906/c5/c5bb1ff6d5c97335a3.img.jpg_200x200_7f63401c.jpg',
        title: '大连生涯海洋世界',
        desc: '浪主题乐园， 唯美海洋动物世界'
      }, {
        id: '0002',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1906/c5/c5bb1ff6d5c97335a3.img.jpg_200x200_7f63401c.jpg',
        title: '大连生涯海洋世界',
        desc: '浪主题乐园， 唯美海洋动物世界'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/sight/p0/1906/c5/c5bb1ff6d5c97335a3.img.jpg_200x200_7f63401c.jpg',
        title: '大连生涯海洋世界',
        desc: '浪主题乐园， 唯美海洋动物世界'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
  @import "~styles/mixins.styl"
  .title
    line-height .8rem
    background #eee
    margin-top .2rem
    text-indent .2rem
  .item
    border-bottom 1px solid #cacaca
    display flex
    height 1.9rem
    overflow hidden
    .item-img
      width 1.7rem
      height 1.7rem
      padding .1rem
    .item-info
      min-width 0
      flex 1
      padding .1rem
      .item-title
        line-height .54rem
        font-size .32rem
        ellipsis()
      .item-desc
        line-height .4rem
        color #ccc
        ellipsis()
      .item-button
        background #ff9300
        line-height .44rem
        color #ffffff
        padding 0 .2rem
        border-radius .06rem
        margin-top .2rem
</style>
