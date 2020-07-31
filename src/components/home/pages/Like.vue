<template>
    <div class="like">
        <div class="like-top">
            <img src="http://img1.qunarzz.com/piao/fusion/1711/89/ebc329f16c55bb02.png" alt="">
            猜你喜欢
        </div>
        <ul>
            <li class="like-item border-bottom"
            v-for='item in likeList'
            :key='item.id'>
                <div class="like-img">
                    <img :src="item.imgUrl" alt="">
                </div>
                <div class="like-text">
                    <div class="like-title">{{item.title}}</div>
                    <div class="like-message">{{item.message}}条评论</div>
                    <div class="like-map">
                        <span class="like-mark">￥<strong>{{item.per}}</strong></span> 起
                        <span class="like-location">{{item.map}}</span>
                    </div>
                </div>
            </li>
        </ul>
    </div>
</template>
<script>
    export default {
        data() {
            return {
                likeList: [{
                    id: '01',
                    imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/b43966c7-9962-4d27-bad8-f649eaba6f3f.jpg_r_480x320x95_e1ea8d63.jpg',
                    title: '长沙-大理 6天跟团游',
                    message: '1341',
                    per: '1880',
                    map: '芙蓉区'
                }, {
                    id: '02',
                    imgUrl: 'https://imgs.qunarzz.com/vs_ceph_vs_tts/896d92f3-e84d-4d5c-bacf-a923d66e14d0.jpg_r_480x320x95_1e605908.jpg',
                    title: '长沙-广西 6天跟团游',
                    message: '1143',
                    per: '2579',
                    map: '雨花区'
                }]
            }
        }
    }
</script>
<style scopeds>
    .like {
        margin-top: .2rem;
        padding: 0 .2rem;
        font-size: .28rem;
        background: #fff;
    }
    
    .like-top {
        padding: .2rem 0;
    }
    
    .like-top img {
        width: .3rem;
        height: .3rem;
    }
    
    .like-item {
        position: relative;
        padding: .2rem;
        overflow: hidden;
    }
    
    .like-img {
        float: left;
    }
    
    .like-img img {
        width: 2rem;
        height: 2rem;
    }
    
    .like-text {
        overflow: hidden;
        padding-left: .2rem;
    }
    
    .like-title {
        font-size: .36rem;
        color: #212121;
    }
    
    .like-message {
        margin-top: .3rem;
        font-size: .24rem;
        color: #616161;
    }
    
    .like-map {
        position: relative;
        margin-top: .3rem;
        color: #616161;
    }
    
    .like-mark {
        color: #ff8300;
    }
    
    .like-mark strong {
        font-size: .4rem;
    }
    
    .like-location {
        position: absolute;
        top: .1rem;
        right: 0;
        font-size: .28rem;
    }
</style>