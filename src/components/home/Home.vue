<template>
    <div class="home">
        <Home-Header></Home-Header>
        <Home-Swiper></Home-Swiper>
        <Home-Icons></Home-Icons>
        <Home-location></Home-location>
        <Home-activity></Home-activity>
        <Home-hot></Home-hot>
        <Home-like></Home-like>
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
    export default {
        components: {
            HomeHeader,
            HomeSwiper,
            HomeIcons,
            HomeLocation,
            HomeActivity,
            HomeHot,
            HomeLike
        }
    }
</script>
<style>
    .home {
        background: #f5f5f5;
    }
</style>