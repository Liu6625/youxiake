<template>
<div ref='container' class="container">
    <div>
        <!-- hot -->
        <div class="hot">
            <div class="hot-title">热门城市</div>
            <ul class="hot-list">
                <li class="hot-item"
                v-for='item in hotCities'
                :key='item.id'>
                    {{item.name}}
                </li>
            </ul>
        </div>
    
        <!-- sort -->
        <div class="sort">
            <div class="sort-title">字母排序</div>
            <ul class="sort-list">
                <li class="sort-item"
                v-for='(val,key) in cities'
                :key='key'
                @click='changeSort(key)'>
                    {{key}}
                </li>
            </ul>
        </div>
        <!-- list -->
        <div class="list">
            <div v-for='(val,key) in cities' 
            :ref='key'
            :key='key'>
                <div class="list-title">{{key}}</div>
                <ul class="list-msg">
                    <li class="list-item"
                    v-for='item in val' 
                    :key='item.id'>
                        {{item.name}}
                    </li>
                </ul>
            </div>
        </div>
    </div>
</div>

</template>
<script>
    import BScroll from '@better-scroll/core'
    // import BScroll from 'better-scroll'
    export default {
        props: ['hotCities', 'cities'],
        data() {
            return {
                scroll: ''
            }
        },
        mounted() {
            let container = this.$refs['container'];
            this.scroll = new BScroll(container);
        },
        methods: {
            changeSort(sortName) {
                this.scroll.scrollToElement(this.$refs[sortName][0]);
                // console.log(this.$refs[sortName][0])
            }
        }
    }
</script>
<style scoped>
    .container {
        position: absolute;
        overflow: hidden;
        left: 0;
        right: 0;
        bottom: 0;
        top: .88rem;
        background: #f5f5f5;
    }
    
    .hot-title {
        font-size: .24rem;
        color: #212121;
        padding: .2rem .3rem;
    }
    
    .hot-list {
        position: relative;
        font-size: .28rem;
        background: #fff;
        overflow: hidden;
        color: #212121;
    }
    
    .hot-list::before {
        content: ' ';
        position: absolute;
        height: 100%;
        width: 33.3333%;
        left: 33.3333%;
        border-left: 1px solid #ddd;
        border-right: 1px solid #ddd;
    }
    
    .hot-item {
        float: left;
        width: 33.3333%;
        height: 0.9rem;
        line-height: 0.9rem;
        text-align: center;
        border-bottom: 1px solid #ddd;
    }
    
    .sort-title {
        font-size: .24rem;
        color: #212121;
        padding: .2rem .3rem;
    }
    
    .sort-list {
        position: relative;
        font-size: .28rem;
        background: #fff;
        overflow: hidden;
        color: #212121;
    }
    
    .sort-item {
        float: left;
        width: 16.6666%;
        height: 0.9rem;
        line-height: 0.9rem;
        text-align: center;
    }
    
    .list-title {
        font-size: .24rem;
        color: #212121;
        padding: .2rem .3rem;
    }
    
    .list-msg {
        position: relative;
        background: #fff;
        overflow: hidden;
    }
    
    .list-msg::before {
        content: '';
        position: absolute;
        left: 25%;
        width: 25%;
        height: 100%;
        border-left: .02rem solid #ddd;
        border-right: .02rem solid #ddd;
    }
    
    .list-msg::after {
        content: '';
        position: absolute;
        left: 75%;
        width: 75%;
        height: 100%;
        border-left: .02rem solid #ddd;
    }
    
    .list-item {
        float: left;
        width: 25%;
        line-height: 0.9rem;
        font-size: .28rem;
        text-align: center;
        border-bottom: .02rem solid #ddd;
        white-space: nowrap;
        text-overflow: ellipsis;
        overflow: hidden;
    }
</style>