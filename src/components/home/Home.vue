<template>
    <div class="home">
        <Home-Header></Home-Header>
        <Home-Swiper></Home-Swiper>
        <Home-Icons></Home-Icons>
        <Home-location></Home-location>
        <Home-activity></Home-activity>
    </div>
</template>
<script>
    import HomeHeader from './pages/Header'
    import HomeSwiper from './pages/Swiper'
    import HomeIcons from './pages/Icons'
    import HomeLocation from './pages/Location'
    import HomeActivity from './pages/Activity'
    export default {
        components: {
            HomeHeader,
            HomeSwiper,
            HomeIcons,
            HomeLocation,
            HomeActivity,
        }
    }
</script>
<style>
    .home {
        background: #f5f5f5;
    }
</style>