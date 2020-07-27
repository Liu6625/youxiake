<template>
    <div class="header-swiper">
        <swiper ref="mySwiper" :options="swiperOptions">
            <swiper-slide v-for='item in swiperList' :key='item.id'>
                <img :src="item.imgUrl" alt="">
            </swiper-slide>
            <div class="swiper-pagination" slot="pagination"></div>
        </swiper>
    </div>    
</template>
<script>
    export default {
        data() {
            return {
                swiperList: [{
                    id: 0,
                    imgUrl: require("@/assets/img/swiper1.jpeg")
                }, {
                    id: 1,
                    imgUrl: require("@/assets/img/swiper2.jpg")
                }, {
                    id: 2,
                    imgUrl: require("@/assets/img/swiper3.jpg")
                }],
                swiperOptions: {
                    pagination: {
                        el: '.swiper-pagination'
                    },
                    loop: true
                }
            }
        }
    }
</script>
<style scoped>
    .header-swiper {
        background: #ccc;
        height: 0;
        padding-bottom: 26.67%;
    }
    
    .header-swiper img {
        width: 100%;
        height: 100%;
    }
</style>