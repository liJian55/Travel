<template>
    <div>
        00
        <home-header :city="city"></home-header>
        <home-swiper :swiperList="swiperList"></home-swiper>
        <HomeIcons :iconList="iconList"></HomeIcons>
        <HomeRecommend :recommendList="recommendList"></HomeRecommend>
        <HomeWeekend :weekendList="weekendList"></HomeWeekend>
        
    </div>
</template>

<script>
import HomeHeader from './components/header'
import HomeSwiper from './components/Swiper'
import HomeIcons from './components/icons'
import HomeRecommend from './components/recommend'
import HomeWeekend from './components/weekend'
import axios from 'axios'
export default {
    name:"home",
    components:{HomeHeader,HomeSwiper,HomeIcons,HomeRecommend,HomeWeekend},
    mounted(){
        this.getHomeInfo()
        },
        data(){
            return{
                city:'北京',
                swiperList:[],
                iconList:[],
                recommendList:[],
                weekendList:[]

            }
        },
        methods:{
            getHomeInfo(){
                axios.get("/api/index.json")
                .then(this.getHomeInfoSucc)
            },
            getHomeInfoSucc(res){
                res = res.data;
                if(res.ret && res.data){
                    const data = res.data
                    this.swiperList = data.swiperList
                    this.iconList = data.iconList
                    this.recommendList = data.recommendList
                    this.weekendList = data.weekendList

                }
                console.log(res)
            }
        }
    }
</script>

<style>

</style>
