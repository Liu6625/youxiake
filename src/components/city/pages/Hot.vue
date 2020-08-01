<template>
    <div class="hot">
        <div class="hot-title">热门城市</div>
        <ul class="hot-list">
            <li class="hot-item">
                北京
            </li>
            <li class="hot-item">
                上海
            </li>
            <li class="hot-item">
                三亚
            </li>
            <li class="hot-item">
                北京
            </li>
            <li class="hot-item">
                上海
            </li>
            <li class="hot-item">
                三亚
            </li>
            <li class="hot-item">
                北京
            </li>
            <li class="hot-item">
                上海
            </li>
            <li class="hot-item">
                三亚
            </li>
        </ul>
    </div>
</template>
<script>
</script>
<style scoped>
    .hot-title {
        font-size: .3rem;
        color: #212121;
        padding: .3rem;
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
</style>