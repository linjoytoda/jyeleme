<template>
    <div class="tab">
        <div class="tab-item">
            <router-link to="/goods">商品</router-link>
        </div>
        <div class="tab-item">
            <router-link to="/ratings">评论</router-link>
        </div>
        <div class="tab-item">
            <router-link to="/seller">商家</router-link>
        </div>
    </div>
</template>
<script>
    export default{}
</script>
<style lang="stylus" rel="stylesheet/stylus">
    @import "../../common/stylus/mixin.styl"
    #app
        .tab
            display:flex
            width:100%
            height:40px
            line-height:40px
            border-1px(rgba(7,17,27,0.1))
            .tab-item
                flex:1
                text-align:center           
</style>