<template>
    <div class="city">
        <city-header></city-header>
        <city-hot :hotCities='hotCities'></city-hot>
        <city-sort :cities='cities'></city-sort>
        <city-list :cities='cities'></city-list>
    </div>
</template>
<script>
    import CityHeader from './pages/Header'
    import CityHot from './pages/Hot'
    import CitySort from './pages/Sort'
    import CityList from './pages/List'
    export default {
        components: {
            CityHeader,
            CityHot,
            CitySort,
            CityList
        },
        data() {
            return {
                hotCities: [],
                cities: {},
            }
        },
        mounted() {
            this.axios.get("http://localhost:8080/static/mock/city.json")
                .then((res) => {
                    let data = res.data.data;
                    this.hotCities = data.hotCities;
                    this.cities = data.cities;
                })
        }
    }
</script>
<style scoped>
    .city {
        background: #f5f5f5;
    }
</style>