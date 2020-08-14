<template>
<div>
    <div class="banner" @click="handleBannerClick">
        <img class="banner-img" src="//img1.qunarzz.com/sight/p0/2003/97/97936710f378de81a3.water.jpg_600x330_f6abb22f.jpg"/>
        <div class="banner-info">
            <div class="banner-title">西樵山国艺影视城</div>
            <div class="banner-number">
                <span class="iconfont banner-icon">&#xe635;</span> 
                4</div>
        </div>
    </div>
    <common-gallary :imgs="imgs" v-show="showGallary" @close="handleGallaryClose"></common-gallary>
</div>
</template>
<script>
import CommonGallary from 'common/gallary/Gallary'
export default{
    name:'DetailBanner',
        data(){
        return{
            showGallary:false,
        imgs:[ "//img1.qunarzz.com/sight/p0/2003/97/97936710f378de81a3.water.jpg_600x330_f6abb22f.jpg",
              'http://img1.qunarzz.com/sight/p0/1510/8e/8eea8eb6f41698290.img.jpg_r_800x800_83a5fe3a.jpg',
              'http://img1.qunarzz.com/sight/p0/1510/ca/ca60a080020329ef90.img.jpg_350x240_9ff2208e.jpg',
              'http://img1.qunarzz.com/sight/p0/1510/cc/ccafbdaac21bdbf790.img.jpg_350x240_c35f8451.jpg'                
                ]
        }
    },
    methods:{
        handleBannerClick(){
            this.showGallary=true 
        },
        handleGallaryClose(){
             this.showGallary=false
        }
    },
    components:{
        CommonGallary
    }
}
</script>
<style lang="stylus" scoped>
.banner
  position:relative
  overflow:hidden
  height:0
  padding-bottom:55%
  .banner-img
    width:100%
  .banner-info
    display:flex
    position:absolute
    left:0
    right:0
    bottom:0
    line-height:.6rem 
    color:#fff
    background-image:linear-gradient(top,rgba(0,0,0,0),rgba(0,0,0,0.8))
    .banner-title
      flex:1
      font-size:.32rem
      padding:0 .2rem
    .banner-number
      margin-top:.14rem
      padding:0 .4rem
      height:.32rem
      line-height:.32rem
      border-radius: 0.2rem
      background:rgba(0,0,0,.8)
      font-size:.24rem
      .banner-icon
        font-size:.24rem
</style>