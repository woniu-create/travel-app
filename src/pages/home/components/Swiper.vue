 <template>
  <div class="wrapper">
  <swiper ref="mySwiper" :options="swiperOptions">
    <swiper-slide v-for="item of swiperList" :key="item.id"> 
        <img class="swiper-img" :src="item.imgUrl"/>
    </swiper-slide>
    <div class="swiper-pagination" slot="pagination"></div>
    <!-- <div class="swiper-button-prev" slot="button-prev"></div>
    <div class="swiper-button-next" slot="button-next"></div> -->
  </swiper>
  </div>
</template>

<script>
  export default {
    name: 'HomeSwiper',
    data() {
      return {
        swiperOptions: {
         pagination:'.swiper-pagination',
         loop:true
        },
        swiperList:[{
            id:'0001',
            imgUrl:'https://imgs.qunarzz.com/sight/p0/2005/30/307fa37039eab5cba3.water.jpg_710x360_9d01c506.jpg'
        },{
             id:'0002',
            imgUrl:'http://imgs.qunarzz.com/sight/p0/1806/d0/d033ab35c038b7c4a3.img.jpg_256x160_b4b0587c.jpg'
        },
        {
             id:'0003',
            imgUrl:'https://imgs.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_710x360_7486df6c.jpg'
        },
        {
             id:'0004',
            imgUrl:'http://imgs.qunarzz.com/sight/p0/1806/d0/d033ab35c038b7c4a3.img.jpg_256x160_b4b0587c.jpg'
        }]
      }
    },
  }
</script>
<style lang="stylus" scoped> 
   .swiper-img
     width: 100% 
     height: 120px

</style>
