<template>
  <div class=wrapper>
    <swiper :options="swiperOption" v-if="showSwiper">
      <swiper-slide v-for='item of list' :key='item.id'>
        <img class='swiper-img' :src=item.imgUrl>
      </swiper-slide>
    </swiper>
  </div>
</template>

<script>
export default {
  name: 'HomeSwiper',
  props: {
    list: Array
  },
  data() {
    return {
      swiperOption: {
        pagination: '.swiper-pagination',
        loop: true
      }
    }
  },
  computed: {
    showSwiper() {
      return this.list.length
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
