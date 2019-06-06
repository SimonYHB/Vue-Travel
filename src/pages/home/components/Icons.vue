<template>
    <div class='icons'>
      <swiper>
          <swiper-slide v-for='(page, index) of pages' :key='index'>
              <div class="icon" v-for='item of page' :key='item.id'>
                <img class='icon-img' :src="item.imgUrl" alt="">
                <p class='icon-p'>{{item.desc}}</p>
              </div>
          </swiper-slide>
      </swiper>
    </div>
</template>

<script>
export default {
  name: 'HomeIcons',
  props: {
    list: Array
  },
  data() {
    return {
      swiperOption: {
        autoplay: false
      }
    }
  },
  computed: {
    pages() {
      const pages = []
      this.list.forEach((item, index) => {
        const page = Math.floor(index / 8)
        if (!pages[page]) {
          pages[page] = []
        }
        pages[page].push(item)
      })
      return pages
    }
  }
}
</script>

<style lang="stylus" scoped>

  .icons
    overflow : hidden
    height: 0
    padding-bottom: 50%
    margin-top: 0
    .icon
      position: relative
      overflow: hidden
      float: left
      width: 25%
      padding-bottom: 25%
      .icon-img
        position: absolute
        margin: 0 auto
        display: block
        width: 60%
        height: 60%
        left: 0
        right: 0
        bottom: .60rem
      .icon-p
        position: absolute
        overflow: hidden
        white-space: nowrap
        text-align: center
        line-height: .44rem
        height: .44rem
        bottom: 0
        left: 0
        right: 0
</style>
