<template>
<div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <home-icons></home-icons>
    <home-recommend></home-recommend>
    
</div>
    
    
</template>

<script>
import HomeHeader from './components/Header.vue'
import HomeSwiper from './components/Swiper.vue'
import HomeIcons from './components/Icons.vue'
import HomeRecommend from './components/Recommend.vue'


export default {
    name: 'Home',
    components: {
        'home-header': HomeHeader,
        'home-swiper': HomeSwiper,
        'home-icons': HomeIcons,
        'home-recommend': HomeRecommend
    }
}
</script>

<style lang="stylus" scoped>


</style>

