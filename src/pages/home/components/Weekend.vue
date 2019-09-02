<template>
    <div>
        <div class="title">周末去哪</div>
        <ul>
            <li class="item border-bottom" v-for="item of list" :key="item.id">
                <div class="item-img-wrapper">
                    <img class="item-img" :src="item.imgUrl" alt="">
                </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>
<script>
export default {
    name: 'HomeWeekend',
    props: {
        list: Array
    },
    data() {
        return {

        }
    },
}
</script>
<style lang="stylus" scoped>
@import '~styles/mixins.styl'
.title
    line-height .8rem
    background #cccccc
    text-indent .2rem
.item-img-wrapper
    height 0
    overflow hidden
    padding-bottom 37.09%
    .item-img
        width 100%
.item-info
    min-width 0
    .item-title
        overflow: hidden;
        padding-left: .2rem;
        color: #212121;
        font-size: .28rem;
        line-height: .48rem;
        white-space: nowrap;
        text-overflow: ellipsis;
        ellipsis()
    .item-desc
        line-height .4rem
        padding-left: .2rem;
        color: #616161;
        font-size: .24rem;
        line-height: .42rem;
        white-space: nowrap;
        color: #616161;
        ellipsis()
</style>
