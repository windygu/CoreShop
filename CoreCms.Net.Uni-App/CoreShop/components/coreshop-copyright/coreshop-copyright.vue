<template>
    <view class="coreshop-copyright">
        <view class="u-font-xs" v-if="shopName">
            © {{shopName}} 版权所有
        </view>
        <view class="beian u-font-xs" v-if="shopBeiAn">
            <view v-if="shopBeian"><a href="http://beian.miit.gov.cn/" target="_blank" style="font-size:24upx">备案号：{{shopBeiAn}}</a></view>
        </view>
    </view>
</template>

<script>
    export default {
        data() {
            return {
                shopBeiAn: this.$store.state.config.shopBeian || '',
                shopName: this.$store.state.config.shopName || ''
            }
        }
    }
</script>
<style scoped lang="scss">
</style>
