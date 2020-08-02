<template>
    <div class="sort">
        <div class="sort-title">字母排序</div>
        <ul class="sort-list">
            <li class="sort-item"
            v-for='(val,key) in cities'
            :key='key'>
                {{key}}
            </li>
        </ul>
    </div>
</template>
<script>
    export default {
        props: ['cities']
    }
</script>
<style scoped>
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
</style>