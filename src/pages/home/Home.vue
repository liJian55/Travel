<template>
    <div>
        <home-header></home-header>
        <home-swiper></home-swiper>
        <HomeIcons></HomeIcons>
    </div>
</template>

<script>
import HomeHeader from './components/header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/icons'
export default {
    name:"home",
    components:{HomeHeader,HomeSwiper,HomeIcons}
    }
</script>

<style>

</style>
