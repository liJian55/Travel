<template>
    <div>
        <home-header></home-header>
        <home-swiper></home-swiper>
        <HomeIcons></HomeIcons>
        
        <HomeRecommend></HomeRecommend>
        <HomeWeekend></HomeWeekend>
        
    </div>
</template>

<script>
import HomeHeader from './components/header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/icons'
import HomeRecommend from './components/recommend'
import HomeWeekend from './components/weekend'
export default {
    name:"home",
    components:{HomeHeader,HomeSwiper,HomeIcons,HomeRecommend,HomeWeekend}
    }
</script>

<style>

</style>
