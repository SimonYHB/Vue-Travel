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
  data() {
    return {
      iconList: [{
        id: '0001',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
        desc: '01'
      }, {
        id: '0002',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20195/b0026eb6f96fd2daecba0d7982c7e4c8.png',
        desc: '02'
      }, {
        id: '0003',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
        desc: '03'
      }, {
        id: '0004',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/bda58ffc3016edad84e656e8a94b0321.png',
        desc: '04'
      }, {
        id: '0005',
        imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20194/cba147cf6cfcea7109d0bff6aac6f626.png',
        desc: '05'
      }, {
        id: '0006',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/a6/6d97515091789602.png',
        desc: '06'
      }, {
        id: '0007',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
        desc: '07'
      }, {
        id: '0008',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
        desc: '08'
      }, {
        id: '0009',
        imgUrl: 'http://img1.qunarzz.com/piao/fusion/1803/b6/37560ece9c62b502.png',
        desc: '09'
      }

      ]
    }
  },
  computed: {
    pages() {
      const pages = []
      this.iconList.forEach((item, index) => {
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
