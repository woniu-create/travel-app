<template>
<div class="header">
   <div class="header-left">
    <div class="iconfont back-icon">&#xe697;</div>
   </div>
   <div class="header-input">
    <span class="iconfont">&#xe6ac;</span>   
       输入要搜索的城市
    </div>
   <div class="header-right">
    城市
    <span class="iconfont arrow-icon">&#xe64a;</span>  
    </div>
</div>
</template>
<script>
export default {
  name: 'Header'
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .header
    display flex
    height: 0.86rem
    line-height:0.86rem
    background: $bgColor
    color:#fff
    .header-left
      .back-icon
        text-align:center
        font-size:.4rem
      width: 0.64rem
      float: left
      text-align:center
    .header-input
      flex:1
      height:0.64rem
      line-height :0.64rem
      margin-top:.12rem
      margin-left:.2rem
      background:#fff
      border-radius:.1rem
      color:#ccc
      padding-left:.2rem
    .header-right
      width:1.24rem
      float:right
      text-align:center
        
</style>

