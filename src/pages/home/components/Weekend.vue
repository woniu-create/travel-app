<template>
<div>
    <div class="title">周末去哪儿</div>
    <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
            <div class="item-img-wrapper">
            <img class="item-img" :src='item.imgUrl' alt="">
            </div>
            <div class="item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
            </div>
        </li>
    </ul>
</div>
</template>
<script>
export default{
    name:'HomeWeekend',
    data(){
        return {
recommendList:[{
            id:'0001',
            imgUrl:'//tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/fd16ccffb2e2376ff370bda3bebebd71.jpg',
            title:'探访日本，一部家庭旅行画册',
            desc:'探访日本，一部家庭旅行画册'
        },
        {
            id:'0002',
            imgUrl:'//tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/fd16ccffb2e2376ff370bda3bebebd71.jpg',
            title:'探访日本，一部家庭旅行画册',
            desc:'探访日本，一部家庭旅行画册'
        },
        {
            id:'0003',
            imgUrl:'//tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/fd16ccffb2e2376ff370bda3bebebd71.jpg',
            title:'探访日本，一部家庭旅行画册',
            desc:'探访日本，一部家庭旅行画册'
        },
        {
            id:'0004',
            imgUrl:'//tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/fd16ccffb2e2376ff370bda3bebebd71.jpg',
            title:'探访日本，一部家庭旅行画册',
            desc:'探访日本，一部家庭旅行画册'
        },
        {
            id:'0005',
            imgUrl:'//tr-osdcp.qunarzz.com/tr-osd-tr-manager/img/fd16ccffb2e2376ff370bda3bebebd71.jpg',
            title:'探访日本，一部家庭旅行画册',
            desc:'探访日本，一部家庭旅行画册'
        }
        ]
        }
    }
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.title
  margin-top : .2rem
  line-height:.8rem
  background:#eee
  text-indent:.2rem
.item-img-wrapper
  overflow:hidden
  height:0
  padding-bottom:33.9%
  .item-img
    width:100%
.item-info
  min-width:0
  flex:1
  padding:.1rem
  .item-title
    line-height:.54rem
    font-size:.32rem
    ellipsisi()
  .item-desc
    line-height: .4rem
    color:#ccc
    ellipsisi()

</style>