<template>
  <div class="list" ref="wrapper">
    <div>
      <div class="area">
          <div class="title border-topbottom">当前城市</div>
          <div class="button-list">
              <div class="button-wrapper">
                  <div class="button">{{this.currentCity}}</div>
            </div>
          </div>
     </div>
      <div class="area">
          <div class="title border-topbottom">热门城市</div>
          <div class="button-list">
              <div class="button-wrapper" v-for="item of hot" :key="item.id" @click="handleCityClick(item.name)">
                  <div class="button">{{item.name}}</div>
             </div>
          </div>
     </div>
          <div class="area" v-for="(item,key) of cities" :key="key" :ref="key">
          <div class="title border-topbottom">{{key}}</div>
          <div class="item-list">
          <div class="item border-bottom" v-for="innerItem of item" :key="innerItem.id"
           @click="handleCityClick(innerItem.name)">{{innerItem.name}}</div>
          </div>
     </div>
  </div>
  </div>
</template>
<script>
import BScroll from 'better-scroll'
import {mapState,mapMutations} from 'vuex'
export default {
    name:'CityList',
    props:{
     hot:Array,
     cities:Object,
     letter:String
    },
    computed:{
      ...mapState({
        currentCity:'city'
      })
    },
    methods:{
      handleCityClick(city){
      // this.$store.commit('changeCity',city)
        this.changeCity(city)
         this.$router.push('/')
      },
      ...mapMutations(['changeCity'])
    },
    mounted() {
      this.scroll=new BScroll(this.$refs.wrapper)
    },
    watch:{
      letter(){
        if(this.letter){
          const element=this.$refs[this.letter][0]
          this.scroll.scrollToElement(element)
        }
      }
    }
}
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl';
  .border-topbottom
    &:before
      border-color #ccc
    &:after
      border-color #ccc
  .border-bottom
  &:before
    border-color #ccc
  .list
    overflow hidden
    position absolute
    top 1.58rem
    right 0
    bottom 0
    left 0
    .title
      line-height .54rem
      padding-left .2rem
      background #eee
      color #666
      font-size .26rem
    .button-list
      padding .1rem .6rem .1rem .1rem
      overflow hidden
      .button-wrapper
        float left
        padding .1rem
        .button
          text-align center
          margin .1rem
          border .02rem solid #ccc
          border-radius .06rem
          padding .1rem .5rem
    .item-list
      .item
        line-height .76rem
        padding-left .2rem

</style>