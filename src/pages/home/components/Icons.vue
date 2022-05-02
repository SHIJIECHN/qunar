<template>
  <div class="icons-wrapper">
        <swiper :options="swiperOption">
            <!-- slides -->
            <swiper-slide v-for="(page, idx) in pages" :key="idx">
            
                <div class="icon-box" v-for="item in page" :key="item.id">
                    <div class="icon-img-box">
                        <img class="icon-img" :src="item.imgUrl" alt="" />
                        
                    </div>
                    <p class="icon-desc">{{item.desc}}</p>
                </div>
            </swiper-slide>
            <!-- Optional controls -->
            <div class="swiper-pagination"  slot="pagination"></div>
            <!-- <swiper-slide >
            
                <div class="icon-box">
                    <div class="icon-img-box">
                        <img class="icon-img" src="https://dummyimage.com/165x165/65372c/fff" alt="" />
                        
                    </div>
                    <p class="icon-desc">景点门票</p>
                </div>
            </swiper-slide> -->
            <!-- Optional controls -->
            <div class="swiper-pagination"  slot="pagination"></div>
        </swiper>
  </div>
</template>

<script>
export default {
    name: "Icons",
  data () {
    return {
        swiperOption: {
            autoplay: false,
            loop: true
        },
        iconsList: [
            {
                id: '001',
                imgUrl: 'https://dummyimage.com/165x165/65372c/fff',
                desc: '景点门票'
            },
            {
                id: '002',
                imgUrl: 'https://dummyimage.com/165x165/39282c/fff',
                desc: '一日游'
            },
            {
                id: '003',
                imgUrl: 'https://dummyimage.com/165x165/098273/fff',
                desc: '长沙必玩'
            },
            {
                id: '004',
                imgUrl: 'https://dummyimage.com/165x165/653920/fff',
                desc: '踏青赏花'
            },
            {
                id: '005',
                imgUrl: 'https://dummyimage.com/165x165/a2039c/fff',
                desc: '游乐场'
            },
            {
                id: '006',
                imgUrl: 'https://dummyimage.com/165x165/645789/fff',
                desc: '动植物园'
            },
            {
                id: '007',
                imgUrl: 'https://dummyimage.com/165x165/65cccc/fff',
                desc: '自然风光'
            },
            {
                id: '008',
                imgUrl: 'https://dummyimage.com/165x165/24572c/fff',
                desc: '湘西凤凰'
            },
            {
                id: '009',
                imgUrl: 'https://dummyimage.com/165x165/ffa456/fff',
                desc: '橘子洲'
            },
            {
                id: '010',
                imgUrl: 'https://dummyimage.com/165x165/bb238c/fff',
                desc: '橘子洲'
            },
        ]
    }
  },
  computed: {
      pages(){
          let pages = [];
          this.iconsList.forEach((item, idx)=>{
              let page = Math.floor(idx / 8); // 1,2,3->0, 9,10->1
              if(!pages[page]){
                  pages[page] = [];
              }
              pages[page].push(item)
          })
          return pages;
      }
  }
}
</script>

<style lang="stylus" scoped>
@import '~styles/variables.styl' 
@import '~styles/mixins.styl' 
.icons-wrapper{
    width: 100%;
    height: 0;
    padding-bottom: 50%;
    background-color: #eee;
    overflow: hidden;
    margin: .2rem 0;
}

.icons-wrapper .icon-box{
    position: relative;
    float: left;
    width: 25%;
    height: 0;
    padding-bottom: 25%;
}

.icons-wrapper .icon-box .icon-img-box{
    position: absolute;
    top: 0;
    left: 0
    right: 0;
    bottom: .44rem;
}

.icons-wrapper .icon-box .icon-img-box .icon-img{
    display: block;
    height: 100%;
    margin: 0 auto;
}

.icons-wrapper .icon-box .icon-desc{
    position: absolute;
    bottom: 0;
    right: 0;
    left: 0;
    height: .44rem;
    line-height: .44rem;
    text-align: center;
    color: $darkTxtColor;
    ellipsis();
}
</style>