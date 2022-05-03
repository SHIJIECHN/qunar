<template>
  <div class="list" ref="listWrapper">
    <div>
      <div class="hot-cities">
        <div class="hot-cts-title">热门城市</div>
        <ul class="clearfix">
          <li>北京</li>
          <li class="border-left">北京</li>
          <li class="border-left">北京</li>
          <li class="border-top">北京</li>
          <li class="border-topleft">北京</li>
          <li class="border-topleft">北京</li>
          <li class="border-top">北京</li>
          <li class="border-topleft">北京</li>
          <li class="border-topleft">北京</li>
          <li class="border-top">北京</li>
          <li class="border-topleft">北京</li>
          <li class="border-topleft">北京</li>
          
        </ul>
      </div>
      <div class="alphabet-menu">
        <div class="alphabet-menu-title">字母排序</div>
        <ul class="clearfix">
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
          <li>A</li>
        </ul>
      </div>
      <div class="alphabet-list">
        <div class="alphabet-list-title">A</div>
        <ul class="clearfix">
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
          </ul>
      </div>
      <div class="alphabet-list">
        <div class="alphabet-list-title">A</div>
        <ul class="clearfix">
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
            <li>阿拉尔</li>
          </ul>
      </div>
    </div>
  </div>
</template>

<script>
import BScroll from 'better-scroll'

export default {
  name: 'CityList',
  data () {
    return {

    };
  },
  mounted(){
    this.scroll = new BScroll(this.$refs.listWrapper);
  }
}
</script>
<style lang="stylus" scoped>
@import '~styles/variables.styl';
div{
  box-sizing: border-box;
}
.clearfix::after {
	display: block;
	content: "";
	clear: both;
}

.list{
  position: absolute;
  top: .88rem;
  left: 0;
  right: 0;
  bottom: 0;  
  overflow: hidden
}

.hot-cities{
  width: 100%;
  height: 4.32rem;
}

.hot-cities .hot-cts-title, 
.alphabet-menu .alphabet-menu-title,
.alphabet-list .alphabet-list-title{
  width: 100%;
  height: .72rem;
  line-height: .72rem;
  padding: 0 .2rem;
  background-color: #f5f5f5;
}

.hot-cities .hot-cts-title{
  width: 100%;
  height .72rem;
  line-height: .72rem;
  padding: 0 .2rem;
  font-size: .26rem;
  color: $lightTxtColor;
}

.hot-cities ul li{
  float: left;
  width: 33.33%;
  height: .9rem;
  line-height: .9rem;
  text-align: center;
}

.alphabet-menu ul{
  height: 4.2rem;
  margin: .3rem 0;  
}

.alphabet-menu ul li{
  float: left;
  width: 16.66%;
  height: .9rem;
  line-height: .9rem;
  text-align: center;
}
.alphabet-list ul li{
  float: left;
  width: 25%;
  height: .9rem;
  line-height: .9rem;
  text-align: center; 
}


  
</style>