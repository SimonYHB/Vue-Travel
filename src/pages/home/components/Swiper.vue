<template>
  <div class=wrapper>
    <swiper :options="swiperOption" ref="mySwiper" @someSwiperEvent="callback">
      <swiper-slide v-for='item of swiperList' :key='item.id'>
        <img class='swiper-img' :src=item.imgUrl>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  data() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      },
      swiperList: [{
        id: '0001',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20193/87a224d0349d94a11e97f31aa1aba4f5.jpg_750x200_1f78af87.jpg'
      }, {
        id: '0002',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/2d971885c2a646dd20a55acce76efd35.jpg_750x200_c66112a8.jpg'
      }]
    }
  }
}
</script>

<style lang="stylus" scoped>
/*  >>>表示表头 wrapper下的子组件 */
  .wrapper >>> .swiper-pagination-bullet-active
    background: #ffffff
  .wrapper
  overflow hidden
    width 100%
    height 0
    padding-bottom 31.25%
    .swiper-img
      width 100%
</style>
