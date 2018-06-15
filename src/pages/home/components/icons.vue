<template>
    <div class="icons">
        <swiper>
            <swiper-slide v-for="(page,index) in pages" :key="index">
                    <div class="icon" v-for="item in page" :key="item.id">
                        <div class="icon-img">
                            <img class="icon-img-content" :src="item.imgUrl" alt="">
                        </div>
                        <p class="icon-desc">{{item.desc}}</p>
                    </div>
                  </swiper-slide>


                
        </swiper>
    </div>
</template>
<script>
export default {
  name: "HomeIcons",
  data() {
    return {
      iconList:[{
          id:'0001',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/95/f3dd6c383aeb3b02.png',
          desc:'景点门票'
      },{
          id:'0002',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/ff/fdf170ee89594b02.png',
          desc:'必游榜单'
      },{
           id:'0003',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/76/eb88861d78fb9902.png',
          desc:'动植物园'
      },{
           id:'0004',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/54/35899492b1302802.png',
          desc:'公园'
      },{
           id:'0005',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/89/55083b0f1951f302.png',
          desc:'游船游艇'
      },{
           id:'0006',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/6a/45f595250c73d102.png',
          desc:'夏日玩水'
      },{
           id:'0007',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/20/831d62d2e1c7be02.png',
          desc:'名胜古迹'
      },{
           id:'0008',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1804/5a/13ceb38dcf262f02.png',
          desc:'一日游'
      },{
           id:'0009',
          imgUrl:'http://img1.qunarzz.com/piao/fusion/1803/b1/528a9e80403b8c02.png',
          desc:'玩转长隆'
      }]
    };
  },
  computed:{
      pages(){
          const pages = [];
          this.iconList.forEach((item,index) =>{
              const page = Math.floor(index/8)
              if(!pages[page]){
                  pages[page] = []
              }
              pages[page].push(item)
          })
          return pages
      }
  }
};
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl';
@import '~styles/mixins.styl';

.icons >>>.swiper-container
    height:0
    padding-bottom:50%


.icon {
    float: left;
    width: 25%;
    height: 0;
    padding-bottom: 25%;
    overflow: hidden;
    position: relative;


    .icon-img {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
        bottom: 0.44rem;
        box-sizing: border-box;
        padding:.1rem

        .icon-img-content {
            height: 100%;
            display: block;
            margin: 0 auto;
        }
    }

    .icon-desc {
        position: absolute;
        left: 0;
        right: 0;
        bottom: 0;
        line-height: 0.44rem;
        height: 0.44rem;
        text-align: center;
        color: $darkTextColor;
        ellipsis()
    }
    }

</style>
