<template>
  <div class="wrapper">
       <swiper :options="swiperOption" v-if="showSwiper">
        <swiper-slide v-for="item in swiperList" :key="item.id">
        <img class="swiperImg" :src="item.imgUrl">
        </swiper-slide>

    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
  </div>
</template>

<script>
export default {
name:"HomeSwiper",
props:{
    swiperList:Array
},
data:function (){
    return{
        swiperOption:{
            pagination:'.swiper-pagination',
            loop:true,
            autoplay:5000
        }
       
    }
},
computed:{
    showSwiper(){
        return this.swiperList.length
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
