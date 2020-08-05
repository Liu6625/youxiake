<template>
    <div>
        <detail-banner></detail-banner>
        <detail-header></detail-header>
        <div style="height: 3000px;"></div>
    </div>
</template>、
<script>
    import DetailBanner from './pages/Banner'
    import DetailHeader from './pages/Header'
    export default {
        components: {
            DetailBanner,
            DetailHeader
        }
    }
</script>
<style scoped>

</style>