<template>
    <div class='header'>
        <div class='header-left'>
            <div class='iconfont back-icon'>&#xe624;</div>
        </div>
        <div class='header-input'>
            <span class='iconfont'>&#xe632;</span>
            输入城市/景点/游玩/主题
        </div>
        <router-link to='/city'>
            <div class='header-right'>
              {{city}}
              <span class='iconfont arrow-icon'>&#xe62d;</span>
            </div>
        </router-link>
    </div>
</template>
<script>
export default {
  name: 'HomeHeader',
  props: {
    city: String
  }
}
</script>

<style lang='stylus' scoped>
    @import '~styles/varibles.styl'
    .header
        display: flex
        align-items: center
        height: .86
        background: $bgColor
        color: #fff
        .header-left
            width: .64rem
            float:left
            .back-icon
                text-align: center
                font-size: .4rem
        .header-input
            flex:1
            background: #ffffff
            height: .64rem
            line-height: .64rem
            margin-top: .11rem
            margin-bottom: .11rem
            margin-left: .2rem
            border-radius: .1rem
            color: #cccccc
        .header-right
            width: 1.24rem
            float: right
            text-align: center
            color: #ffffff
            .arrow-icon
                font-size: .24rem
                margin-left: -.04rem
</style>
