<template>
    <div class="home">
        <Home-Header></Home-Header>
        <Home-Swiper :swiperList='swiperList'></Home-Swiper>
        <Home-Icons :iconsList='iconsList'></Home-Icons>
        <Home-location></Home-location>
        <Home-activity></Home-activity>
        <Home-hot :hotList='hotList'></Home-hot>
        <Home-like :likeList='likeList'></Home-like>
        <Home-vacation :vacationList='vacationList'></Home-vacation>
    </div>
</template>
<script>
    import {
        mapState
    } from 'vuex'
    import HomeHeader from './pages/Header'
    import HomeSwiper from './pages/Swiper'
    import HomeIcons from './pages/Icons'
    import HomeLocation from './pages/Location'
    import HomeActivity from './pages/Activity'
    import HomeHot from './pages/Hot'
    import HomeLike from './pages/Like'
    import HomeVacation from './pages/Vacation'
    export default {
        components: {
            HomeHeader,
            HomeSwiper,
            HomeIcons,
            HomeLocation,
            HomeActivity,
            HomeHot,
            HomeLike,
            HomeVacation
        },
        data() {
            return {
                swiperList: [],
                iconsList: [],
                hotList: [],
                likeList: [],
                vacationList: [],
                changeCity: ''
            }
        },
        computed: {
            ...mapState(['city'])
        },
        methods: {
            getHttp() {
                this.axios.get("http://localhost:8080/static/mock/dataHome.json")
                    .then((res) => {
                        // console.log(res.data.data[0]);
                        const data = res.data.data;
                        data.forEach((item, index) => {
                            if (item.city == this.city) {
                                this.swiperList = item.swiperList;
                                this.iconsList = item.iconsList;
                                this.hotList = item.hotList;
                                this.likeList = item.likeList;
                                this.vacationList = item.vacationList;
                            } else {
                                this.swiperList = data[0].swiperList;
                                this.iconsList = data[0].iconsList;
                                this.hotList = data[0].hotList;
                                this.likeList = data[0].likeList;
                                this.vacationList = data[0].vacationList;
                            }
                        })

                    })
            }
        },
        mounted() {
            this.changeCity = this.city
            this.getHttp()
        },
        activated() {
            if (this.changeCity != this.city) {
                this.getHttp();
                this.changeCity = this.city;
            }
        }
    }
</script>
<style>
    .home {
        background: #f5f5f5;
    }
</style>