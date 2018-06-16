<template>
    <div>
        <div class="recommend-title">周末去哪儿</div>
        <ul class="">
            <li class="item border-bottom" v-for="item in recommendList" :key="item.id">
                <div class="item-img-wrapper">
                    <img :src="item.imgUrl" class="item-img"/>
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
    name:'weekend',
    data(){
        return{
            recommendList:[{
                id:"0001",
                imgUrl:"http://img1.qunarzz.com/sight/source/1505/92/580e9ea4f37a1b.jpg_r_640x214_72112761.jpg",
                title:"广州必游TOP10",
                desc:"感受现代与传统相融合的广州~"
            },{
                id:"0002",
                imgUrl:"http://img1.qunarzz.com/sight/source/1506/fd/08f524fa9455b4.jpg_r_640x214_b37dbb39.jpg",
                title:"暑期玩转粤港澳",
                desc:"这个假期开启最高大上的国内游~2"
            },{
                id:"0003",
                imgUrl:"http://img1.qunarzz.com/sight/source/1505/50/07fa9343791682.jpg_r_640x214_c8c3d798.jpg",
                title:"自然户外好去处",
                desc:"快快来到户外，感受花城的魅力~3"
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
    .item.img-wrapper
        overflow:hidden;
        height:0;
        padding-bottom:33.9%
    .item-img
          width:100%
    .item-info
        padding:.1rem;
        .item-title
            line-height:.54rem;
            font-size:.32rem;
            ellipsis()
        .item-desc
            line-height:.4rem;
            color:#ccc;
            ellipsis()
                



            




</style>
