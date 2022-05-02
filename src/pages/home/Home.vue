<template>
<div>
    <home-header></home-header>
    <home-swiper></home-swiper>
    <icons></icons>
    
</div>
    
    
</template>

<script>
import HomeHeader from './components/Header.vue'
import HomeSwiper from './components/Swiper.vue'
import Icons from './components/Icons.vue'

export default {
    name: 'Home',
    components: {
        'home-header': HomeHeader,
        'home-swiper': HomeSwiper,
        'icons': Icons
    }
}
</script>

<style lang="stylus" scoped>


</style>

