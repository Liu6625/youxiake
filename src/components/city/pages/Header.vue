<template>
    <div class="header">
        <div class="header-left" @click='toHome'>
            <span class='iconfont'>
				&#xe624;
			</span>
        </div>
        <div class="header-title">
            城市选择
        </div>
    </div>
</template>
<script>
    export default {
        methods: {
            toHome() {
                this.$router.push('/')
            }
        }
    }
</script>
<style scoped lang="stylus">
    @import '~css/var.styl';
    /* 在style中加，在js中不用加 */
    
    .header {
        position: relative;
        width: 100%;
        line-height: .88rem;
        height: 0.88rem;
        background: $bgColor;
        color: $textColor;
        font-size: .32rem;
    }
    
    .header-left {
        position: absolute;
        width: .4rem;
        padding: 0 .2rem;
        text-align: center;
        font-weight: bold;
    }
    
    .header-title {
        text-align: center;
    }
</style>