<template>
<div>
    <home-header :city=city></home-header>
    <home-swiper :swiper-list = swiperList></home-swiper>
    <home-icons :icons-list = iconsList></home-icons>
    <home-recommend :recommend-list=recommendList></home-recommend>
    <home-weekend :weekend-list=weekendList></home-weekend>

    
</div>
    
    
</template>

<script>
import HomeHeader from './components/Header.vue'
import HomeSwiper from './components/Swiper.vue'
import HomeIcons from './components/Icons.vue'
import HomeRecommend from './components/Recommend.vue'
import HomeWeekend from './components/Weekend.vue'
import axios from 'axios'


export default {
    name: 'Home',
    components: {
        'home-header': HomeHeader,
        'home-swiper': HomeSwiper,
        'home-icons': HomeIcons,
        'home-recommend': HomeRecommend,
        'home-weekend': HomeWeekend
    },
    data(){
        return {
            city: '',
            swiperList: [],
            iconsList: [],
            recommendList: [],
            weekendList: []
        }
    },
    methods:{
        getHomeInfo(){
            axios.get('/api/index.json').then(res=>{
                this.getHomeInfoSuccess(res);
            })
        },

        getHomeInfoSuccess(res){
            if(res.data.ret && res.data.data){
                let data = res.data.data;
                this.city = data.city;
                this.swiperList = data.swiperList;
                this.iconsList = data.iconsList;
                this.recommendList = data.recommendList;
                this.weekendList = data.weekendList;
            }
        }
    },
    mounted(){
        this.getHomeInfo();
    }
}
</script>

<style lang="stylus" scoped>


</style>

