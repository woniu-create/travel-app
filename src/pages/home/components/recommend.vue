<template>
<div>
    <div class="title">热销推荐</div>
    <ul>
        <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
            <img class="item-img" :src='item.imgUrl' alt="">
            <div class="item-info">
                <p class="item-title">{{item.title}}</p>
                <p class="item-desc">{{item.desc}}</p>
                <button class="item-button">查看详情</button>
            </div>
        </li>
    </ul>
</div>
</template>
<script>
export default{
    name:'HomeRecommend',
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
.item
  overflow:hidden
  display:flex
  height:1.9rem
  .item-img
    width:1.7rem
    height:1.7rem
    padding:.1rem
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
    .item-button
      line-height:.44rem
      margin-top:.2rem
      background:#ff9300
      padding:0 .2rem
      border-radius:.06rem
      color:#fff
</style>