<template>
    <div>
        <div class="recommend-title">热销推荐</div>
        <ul class="">
            <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
                <img :src="item.imgUrl" class="item-img"/>
        
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <button class="item-button">查看详情哦</button>
                </div>
            </li>
        </ul>
    </div>
</template>
<script>
export default{
    name:'recommend',
    props:{
        recommendList:Array
    },
    data(){
        return{
          
        }
    }

}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl'
    .recommend-title
        margin-top:.2rem
        line-height:.8rem;
        text-indent:.2rem;
    .item
        display:flex;
        overflow:hidden;
        height:1.9rem;
        .item-img
            width:1.7rem;
            height:1.7rem;
            padding:.1rem;
        .item-info
            flex:1
            padding:.1rem;
            min-width:0
            .item-title
                line-height:.54rem;
                font-size:.32rem;
                ellipsis()
            .item-desc
                line-height:.4rem;
                color:#ccc;
                ellipsis()
                
            .item-button
                line-height:.44rem;
                margin-top:.16rem;
                background:#ff9300;
                padding:0 .2rem;
                border-radius:.06rem;
                border:none;
                color:#fff



            




</style>
