<template>
<div class="header">
   <div class="header-left">
    <div class="iconfont back-icon">&#xe697;</div>
   </div>
   <div class="header-input">
    <span class="iconfont">&#xe6ac;</span>   
       输入要搜索的城市
    </div>
    <router-link to='/city'>
   <div class="header-right">
   {{this.city}}
    <span class="iconfont arrow-icon">&#xe64a;</span>  
    </div>
    </router-link>
</div>
</template>
<script>
import {mapState} from 'vuex'
export default {
  name: 'Header',
  computed:{
    ...mapState(['city'])
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl'
  .header
    display flex
    height:$headerHeight
    line-height:$headerHeight
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
      min-width:0 .1rem
      float:right
      text-align:center
      color:#fff

        
</style>

