<template>
<div>
<<<<<<< HEAD
<home-header :city="city"></home-header>
<home-swiper :list="swiperList"></home-swiper>
<home-icon :list="iconList"></home-icon>
<home-recommend :list="recommendList"></home-recommend>
<home-weekend :list="weekendList"></home-weekend>
<<<<<<< HEAD
=======
=======
<home-header :city="city"></home-header>
<home-swiper :list="swiperList"></home-swiper>
<home-icon :list="iconList"></home-icon>
<home-recommend :list="recommendList"></home-recommend>
<home-weekend :list="weekendList"></home-weekend>
>>>>>>> index-ajax

>>>>>>> index-recommend
</div>
</template>
<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
import HomeIcon from './components/Icon'
<<<<<<< HEAD
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
<<<<<<< HEAD
=======
import HomeRecommend from './components/Recommend'
import HomeWeekend from './components/Weekend'
>>>>>>> index-recommend
=======
import HomeRecommend from './components/recommend'
import axios from 'axios'
>>>>>>> index-ajax
export default {
  name: 'Home',
  components:{
      HomeHeader,
      HomeSwiper,
      HomeIcon,
      HomeRecommend,
<<<<<<< HEAD
      HomeWeekend,
=======
      HomeWeekend,
<<<<<<< HEAD
      
>>>>>>> index-recommend
=======
  },
  data(){
    return{
      city:'',
      swiperList:[],
      iconList:[],
      recommendList:[],
      weekendList:[]
    } 
  },
  methods:{
    getHomeInfo(){
      axios.get('/api/index.json')
        .then(this.getHomeInfoSucc)
    },
    getHomeInfoSucc(res){
      res=res.data
      console.log(res)
      if(res.ret&&res.data){
        const data=res.data
        this.city=data.city
        this.swiperList=data.swiperList
        this.iconList=data.iconList
        this.recommendList=data.recommendList
        this.weekendList=data.weekendList
      }
    }
  },
  mounted(){
    this.getHomeInfo()
>>>>>>> index-ajax
  }
}
</script>

