<template>
    <div class="icons">
        <swiper ref="mySwiper" :options="swiperOptions">
            <swiper-slide 
            v-for='(item,key) in page' 
            :key="key">
                <div class="icons-item" v-for='page in item'>
                    <img :src="page.imgUrl">
                    <p>{{page.title}}</p>
                </div>
            </swiper-slide>
        </swiper>

        
    </div>
</template>
<script>
    export default {
        data() {
            return {
                swiperOptions: {},
                iconsList: [{
                    id: 0,
                    imgUrl: "https://s.qunarzz.com/homenode/images/touchheader/hotel.png",
                    title: "酒店"
                }, {
                    id: 1,
                    imgUrl: "https://s.qunarzz.com/homenode/images/touchheader/hotel.png",
                    title: "酒店"
                }, {
                    id: 2,
                    imgUrl: "https://s.qunarzz.com/homenode/images/touchheader/flight.png",
                    title: "飞机"
                }, {
                    id: 3,
                    imgUrl: "https://s.qunarzz.com/homenode/images/touchheader/hotel.png",
                    title: "酒店"
                }, {
                    id: 4,
                    imgUrl: "https://s.qunarzz.com/homenode/images/touchheader/train.png",
                    title: "火车"
                }, {
                    id: 5,
                    imgUrl: "https://s.qunarzz.com/homenode/images/touchheader/hotel.png",
                    title: "酒店"
                }, {
                    id: 6,
                    imgUrl: "https://s.qunarzz.com/homenode/images/touchheader/package.png",
                    title: "度假"
                }, {
                    id: 7,
                    imgUrl: "https://s.qunarzz.com/homenode/images/touchheader/hotel.png",
                    title: "酒店"
                }, {
                    id: 8,
                    imgUrl: "https://s.qunarzz.com/homenode/images/touchheader/piao.png",
                    title: "景点门票"
                }, {
                    id: 9,
                    imgUrl: "https://s.qunarzz.com/homenode/images/touchheader/hotel.png",
                    title: "酒店"
                }, {
                    id: 10,
                    imgUrl: "https://s.qunarzz.com/homenode/images/touchheader/hotel.png",
                    title: "酒店"
                }]
            }
        },
        computed: {
            page() {
                let pages = [];
                this.iconsList.forEach((item, index) => {
                    let idx = Math.floor(index / 8);
                    if (!pages[idx]) {
                        pages[idx] = []
                    };
                    pages[idx].push(item);

                })
                return pages;
            }
        }
    }
</script>
<style scoped>
    .icons {
        width: 100%;
        margin-top: .2rem;
        background: #fff;
    }
    
    .icons-item {
        float: left;
        width: 25%;
        padding-bottom: 25%;
        height: 0;
    }
    
    .icons-item img {
        width: 1.1rem;
        height: 1.1rem;
        display: block;
        margin: 0 auto;
        padding-top: .2rem;
    }
    
    .icons-item p {
        margin-top: .1rem;
        font-size: .28rem;
        text-align: center;
        color: #212121;
    }
</style>