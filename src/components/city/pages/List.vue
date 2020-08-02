<template>
    <div class="list">
        <div>
            <div class="list-title">A</div>
            <ul class="list-msg">
                <li class="list-item">
                    阿克苏地区
                </li>
                <li class="list-item">
                    阿克苏地区
                </li>
                <li class="list-item">
                    阿克苏地区
                </li>
                <li class="list-item">
                    阿克苏地区
                </li>
                <li class="list-item">
                    阿克苏地区
                </li>
                <li class="list-item">
                    阿被速度快发送
                </li>
                <li class="list-item">
                    阿克苏地区
                </li>
                <li class="list-item">
                    阿克苏地区
                </li>
            </ul>
        </div>
    </div>
</template>
<style scoped>
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