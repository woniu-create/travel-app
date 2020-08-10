<template>
<div>
<home-header></home-header>
<home-swiper></home-swiper>
<home-icon></home-icon>
<home-recommend></home-recommend>
<home-weekend></home-weekend>

</div>
</template>
<script>
import HomeHeader from './components/Header'
import HomeSwiper from './components/Swiper'
// import HomeSwiper from './components/Swiper'
import HomeIcon from './components/Icon'
import HomeWeekend from './components/Weekend'
import HomeRecommend from './components/recommend'
export default {
  name: 'Home',
  components:{
      HomeHeader,
      HomeSwiper,
      HomeIcon,
      HomeRecommend,
      HomeWeekend,
      
  }
}
</script>

