<!-- The ref attr used to find the swiper instance -->
<template>
<div class="sw-wrapper">
   <swiper :options="swiperOption" ref="mySwiper">
    <!-- slides -->
    <swiper-slide v-for="item in swiperList" :key="item.id">
      <img class="swiper-img" :src="item.imgUrl" alt="">
    </swiper-slide>
    <!-- Optional controls -->
    <div class="swiper-pagination"  slot="pagination"></div>
  </swiper>
</div>
</template>

<script>
  // swiper options example:
  export default {
    name: 'HomeSwiper',
    data() {
      return {
       swiperOption: {
         pagination: '.swiper-pagination',
         loop: true,
       },
       swiperList: [
         {
           id: '001',
           imgUrl: 'https://dummyimage.com/750x200/a3a1a3/fff'
         },
         {
           id: '002',
           imgUrl: 'https://dummyimage.com/750x200/0b7841/fff'
         },
         {
           id: '003',
           imgUrl: 'https://dummyimage.com/750x200/4f992c/fff'
         },
         {
           id: '004',
           imgUrl: 'https://dummyimage.com/750x200/992c49/fff'
         },
         {
           id: '005',
           imgUrl: 'https://dummyimage.com/750x200/99952c/fff'
         },
         {
           id: '006',
           imgUrl: 'https://dummyimage.com/750x200/99352c/fff'
         },
       ]
        
      }
    }
  }
</script>

<style lang="stylus" scoped>
.sw-wrapper >>> .swiper-pagination-bullet-active{
  background-color: #fff;
}

.sw-wrapper{
  overflow: hidden;
  width: 100%;
  height: 0;
  padding-bottom: 26.67%;
  background-color: #eee;
}
.sw-wrapper .swiper-img{
  width: 100%;
  height: 100%;
}
</style>