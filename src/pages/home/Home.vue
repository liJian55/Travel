<template>
    <div>
        <home-header></home-header>
        <home-swiper></home-swiper>
        <HomeIcons></HomeIcons>
<<<<<<< HEAD
        
=======
        <HomeRecommend></HomeRecommend>
        <HomeWeekend></HomeWeekend>
>>>>>>> origin/index-recommend
        
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
