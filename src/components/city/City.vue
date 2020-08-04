<template>
    <div class="city">
        <city-header></city-header>
        <city-list 
        :hotCities='hotCities'
        :cities='cities'>
        </city-list>
    </div>
</template>
<script>
    import CityHeader from './pages/Header'
    import CityList from './pages/List'
    export default {
        components: {
            CityHeader,
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