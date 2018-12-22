<template>
    <div class="header">
        <div class="header-left">返回</div>
        <div class="header-input">输入城市/景点/游玩主题</div>
        <div class="header-right">城市</div>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
  .header
    display flex
    line-height .86rem
    background-color #00bcd4
    color #ffffff
    .header-left
      width .64rem
      float left
    .header-right
      width 1.24rem
      float right
      text-align center
    .header-input
      line-height .64rem
      height .64rem
      margin-top .12rem
      margin-left .2rem
      background #ffffff
      border-radius .1rem
      color #cccccc
      flex 1
</style>
