<template>
    <div class="hot">
        <div class="hot-top">
            <img src="http://img1.qunarzz.com/piao/fusion/1711/16/bfbb9874e8f11402.png" alt="">
            <span>本周热门榜单</span>
            <span class="hot-title">全部榜单 ></span>
        </div>
        <ul class="hot-list">
            <li class="hot-item"
            v-for='item in hotList'
            :key='item.id'>
                <img :src="item.imgUrl" alt="">
                <p>{{item.title}}</p>
                <p>
                    <span class="hot-mark">￥{{item.mark}}</span> 起
                </p>
            </li>
        </ul>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                hotList: [{
                    id: '01',
                    imgUrl: 'https://img1.qunarzz.com/sight/p0/1605/58/5847560fd55ff6f590.water.jpg_256x160_13631f57.jpg',
                    title: '凤凰古城',
                    mark: '125'
                }, {
                    id: '02',
                    imgUrl: 'https://img1.qunarzz.com/sight/p79/201211/06/cb2677b88c36471c93835fbb.jpg_256x160_82d0f3bc.jpg',
                    title: '张家界国家森林公园',
                    mark: '215'
                }, {
                    id: '03',
                    imgUrl: 'https://img1.qunarzz.com/sight/p0/1505/c2/c27514a93e8b8392.water.jpg_256x160_b1943551.jpg',
                    title: '东江湖',
                    mark: '80'
                }, {
                    id: '04',
                    imgUrl: 'https://img1.qunarzz.com/sight/p0/1708/43/436d079f7f1df3dda3.water.jpg_256x160_87cfadb4.jpg',
                    title: '天子山索道',
                    mark: '144'
                }, {
                    id: '05',
                    imgUrl: 'https://imgs.qunarzz.com/sight/p0/1905/29/296e5659470d69bea3.img.jpg_256x144_bdea1689.jpg',
                    title: '长沙世界之窗',
                    mark: '95'
                }, {
                    id: '06',
                    imgUrl: 'https://imgs.qunarzz.com/sight/p0/1604/85/8557f0d167c9da5890.img.jpg_256x144_47bb8a04.jpg',
                    title: '张家界大峡谷',
                    mark: '95'
                }, {
                    id: '07',
                    imgUrl: 'https://img1.qunarzz.com/sight/p0/1605/58/5847560fd55ff6f590.water.jpg_256x160_13631f57.jpg',
                    title: '凤凰古城',
                    mark: '125'
                }]
            }
        }
    }
</script>
<style scoped>
    .hot {
        margin-top: .2rem;
        background: #fff;
        font-size: .28rem;
    }
    
    .hot-top {
        position: relative;
        padding: .2rem;
    }
    
    .hot-top img {
        width: .3rem;
        height: .3rem;
    }
    
    .hot-top span {
        color: #212121;
        font-size: .32rem;
    }
    
    .hot-top .hot-title {
        position: absolute;
        right: .2rem;
        color: #616161;
    }
    
    .hot-list {
        height: 3rem;
        overflow-x: scroll;
        overflow-y: hidden;
        white-space: nowrap;
    }
    
    .hot-item {
        display: inline-block;
        padding: 0 .2rem;
        width: 2rem;
        height: 2rem;
    }
    
    .hot-item img {
        width: 100%;
        height: 100%;
    }
    
    .hot-item p {
        margin-top: .1rem;
        text-align: center;
        white-space: nowrap;
        text-overflow: ellipsis;
        overflow: hidden;
    }
    
    .hot-item p .hot-mark {
        color: #ff8300;
        font-size: .32rem;
    }
</style>