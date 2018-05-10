<template>
  <div class="wrapper">
       <swiper :options="swiperOption">
    <!-- slides -->
    <swiper-slide v-for="item in swiperList" :key="item.id"><img class="swiperImg" :src="item.imgUrl"></swiper-slide>
  
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
name:"HomeSwiper",
data:function (){
    return{
        swiperOption:{
            pagination:'.swiper-pagination',
            loop:true
        },
        swiperList:[
            {id:'0001',imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/b1/54862f4b1501e202.jpg_750x200_097bb6b3.jpg'},
            {id:'0002',imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/15/9250dbc86a456302.jpg_750x200_b423f532.jpg'}
            ]
    }
}
 }
</script>

<style lang="stylus" scoped>
.wrapper>>> .swiper-pagination-bullet-active
        background:#fff
.wrapper
    width:100%
    height:0
    overflow:hidden
    padding-bottom:31.25%
    .swiperImg
        width:100%
    .swiper-pagination-bullet-active
        color:#fff
    
</style>
