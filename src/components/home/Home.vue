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
                vacationList: []
            }
        },
        mounted() {
            this.axios.get("http://localhost:8080/static/mock/dataHome.json")
                .then((res) => {
                    // console.log(res.data.data[0]);
                    const data = res.data.data[0];
                    this.swiperList = data.swiperList;
                    this.iconsList = data.iconsList;
                    this.hotList = data.hotList;
                    this.likeList = data.likeList;
                    this.vacationList = data.vacationList;
                })
        }
    }
</script>
<style>
    .home {
        background: #f5f5f5;
    }
</style>