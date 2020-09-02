 <template>
  <div class="wrapper">
  <swiper ref="mySwiper" :options="swiperOptions" v-if="showSwiper ">
    <swiper-slide v-for="item of list" :key="item.id"> 
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
    props:{
      list:Array
    },
    data() {
      return {
        swiperOptions: {
         pagination:'.swiper-pagination',
         loop:true,
         speed: 1000,
         autoplay:2000,
         paginationClickable: true,//点击切换
         autoplayDisableOnInteraction:false,
         preventLinksPropagation:true
        },
      }
    },
    computed:{
      showSwiper(){
        return this.list.length
      }
    }
  }
</script>
<style lang="stylus" scoped> 
   .swiper-img
     width: 100% 
     height: 120px

</style>
