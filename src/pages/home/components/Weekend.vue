<template>
<div>
    <div class="recommend-title">
      周末去哪儿
    </div>
    <ul>
        <router-link
         tag="li"
         class="list-item"
         v-for="item in recommendList"
         :key="item.id"
         to="/detail">
            <div class="item-img">
                <img :src="item.imgUrl" alt="">
            </div>
            <div class="item-info">
                <div class="info-title">{{item.title}}</div>
                <div class="info-comment">{{item.comment}}</div>
            </div>
        </router-link>
    </ul>
</div>
    
</template>

<script>
export default {
    name: 'HomeWeekend',
  data () {
    return {
        recommendList: [
            {
                id: '001',
                imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/15/66f14e0fd6fbb.jpg_r_640x214_5d69f21d.jpg',
                title: '清远周边逛',
                comment: '人人都有一双发现美的眼睛，身边的事物最熟悉不过，那你可曾发现了被人遗漏的美？'
            },
            {
                id: '002',
                imgUrl: 'https://imgs.qunarzz.com/sight/source/1811/f8/29dfa785277839.jpg_r_640x214_7d051523.jpg',
                title: '阳江温泉知多少',
                comment: '这里的天空和大海让人心旷神怡，配上舒缓的优美音乐，泡个暖暖的温泉岂不美哉'
            },
            {
                id: '003',
                imgUrl: 'https://imgs.qunarzz.com/sight/source/1812/47/cbdc44f461db0d.jpg_r_640x214_aab1da76.jpg',
                title: '珠江夜游',
                comment: '绚烂的霓虹将珠江照亮，跳上一艘游船，沉浸在这醉人的夜色中'
            }
        ]
    };
  },
}
</script>
<style lang="stylus" scoped>
@import '~styles/variables.styl'
@import '~styles/mixins.styl'

div{
    box-sizing: border-box;
}
.recommend-title{
    width: 100%;
    height: .8rem;
    line-height: .8rem;
    font-size: .28rem;
    background-color: #eee;
    padding: 0 .2rem; 
}



.list-item .item-img{
    width: 100%;
    height: 0;
    padding-bottom: 37.1%; 
}
.list-item .item-img img{
    width: 100%;
}


.list-item .item-info{
    padding: .14rem .2rem .2rem;
}

.item-info .info-title{
    width: 100%;
    height: .48rem;
    line-height: .48rem;
    font-size: .28rem;
    ellipsis();
}

.item-info .info-comment{
    width: 100%;
    height: .42rem;
    line-height: .28rem;
    font-size: .24rem;
    color: $lightTxtColor;
    ellipsis();
}

</style>