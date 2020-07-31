<template>
    <div>
        <Home-Header></Home-Header>
        <Home-Swiper></Home-Swiper>
        <Home-Icons></Home-Icons>
        <Home-location></Home-location>
    </div>
</template>
<script>
    import HomeHeader from './pages/Header'
    import HomeSwiper from './pages/Swiper'
    import HomeIcons from './pages/Icons'
    import HomeLocation from './pages/Location'
    export default {
        components: {
            HomeHeader,
            HomeSwiper,
            HomeIcons,
            HomeLocation
        }
    }
</script>
<style>

</style>