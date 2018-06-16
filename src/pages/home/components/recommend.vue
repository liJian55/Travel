<template>
    <div>
        <div class="recommend-title">热销推荐</div>
        <ul class="">
            <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
                <img :src="item.imgUrl" class="item-img"/>
        
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
    name:'recommend',
    data(){
        return{
            recommendList:[{
                id:"0001",
                imgUrl:"http://img1.qunarzz.com/sight/p0/1709/41/411f234d79457081a3.img.jpg_200x200_ea02ef99.jpg",
                title:"长隆野生动物世界",
                desc:"来广州来长隆，就对了，就够了~"
            },{
                id:"0002",
                imgUrl:"http://img1.qunarzz.com/sight/p0/1601/3d/3dc7f222d6bca6a790.img.jpg_200x200_e0bb3017.jpg",
                title:"广州花城汇MAG环球魔幻世界",
                desc:"来广州来长隆，就对了，就够了~2"
            },{
                id:"0003",
                imgUrl:"http://img1.qunarzz.com/sight/p0/1507/9e/7b5e0a44cb0310280b1aeb2a8dd94de8.water.jpg_200x200_3c429960.jpg",
                title:"长隆国际大马戏剧院",
                desc:"来广州来长隆，就对了，就够了~3"
            }]
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
