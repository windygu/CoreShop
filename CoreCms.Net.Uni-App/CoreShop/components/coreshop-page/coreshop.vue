<template>
    <view>
        <block v-for="(item,index) in coreshopdata" :key="index">
            <!--�������޸���-->
            <coreshopsearch :coreshopdata="item" v-if="item.widgetCode=='search' "></coreshopsearch>
            <!--�л�-->
            <coreshoptabbar :coreshopdata="item" v-if="item.widgetCode=='tabBar' "></coreshoptabbar>
            <!--���棨�޸���-->
            <coreshopnotice :coreshopdata="item" v-if="item.widgetCode=='notice' "></coreshopnotice>
            <!--ͼƬ�ֲ����޸���-->
            <coreshopimgSlide :coreshopdata="item" v-if="item.widgetCode=='imgSlide' "></coreshopimgSlide>
            <!--�Ż�ȯ���޸���-->
            <coreshopcoupon :coreshopdata="item" v-if="item.widgetCode=='coupon' "></coreshopcoupon>
            <!--�ո��޸���-->
            <coreshopblank :coreshopdata="item" v-if="item.widgetCode=='blank' "></coreshopblank>
            <!--�����ı����������޸���-->
            <coreshoptextarea :coreshopdata="item" v-if="item.widgetCode=='textarea' "></coreshoptextarea>
            <!--��Ƶ���޸���-->
            <coreshopvideo :coreshopdata="item" v-if="item.widgetCode=='video' "></coreshopvideo>
            <!--ͼƬ�����޸���-->
            <coreshopimgWindow :coreshopdata="item" v-if="item.widgetCode=='imgWindow' "></coreshopimgWindow>
            <!--ͼƬ--���޸���-->
            <coreshopimgSingle :coreshopdata="item" v-if="item.widgetCode=='imgSingle' "></coreshopimgSingle>
            <!--��Ʒ���޸���-->
            <coreshopgoods :coreshopdata="item" v-if="item.widgetCode=='goods' "></coreshopgoods>
            <!--���£��޸���-->
            <coreshoparticle :coreshopdata="item" v-if="item.widgetCode=='article' "></coreshoparticle>
            <!--���·��ࣨ�޸���-->
            <coreshoparticleClassify :coreshopdata="item" v-if="item.widgetCode=='articleClassify' "></coreshoparticleClassify>
            <!--�����Զ��嵼�����޸���-->
            <coreshopnavBar :coreshopdata="item" v-if="item.widgetCode=='navBar' "></coreshopnavBar>
            <!--�Ź����޸���-->
            <coreshopgroupPurchase :coreshopdata="item" v-if="item.widgetCode=='groupPurchase' "></coreshopgroupPurchase>
            <!--�����¼���޸���-->
            <coreshoprecord :coreshopdata="item" v-if="item.widgetCode=='record' "></coreshoprecord>
            <!--ƴ�ţ��޸���-->
            <coreshoppinTuan :coreshopdata="item" v-if="item.widgetCode=='pinTuan' "></coreshoppinTuan>
            <!--�����޸���-->
            <coreshopservice :coreshopdata="item" v-if="item.widgetCode=='service' "></coreshopservice>
            <!--�������-->
            <coreshopadpop :coreshopdata="item" v-if="item.widgetCode=='adpop' "></coreshopadpop>
            <!--�ı����ݣ��޸���-->
            <coreshopContent :coreshopdata="item" v-if="item.widgetCode=='content' "></coreshopContent>
        </block>
    </view>
</template>

<script>
    import coreshopimgSlide from '@/components/coreshop-page/coreshop-imgSlide.vue'
    import coreshopsearch from '@/components/coreshop-page/coreshop-search.vue'
    import coreshopnotice from '@/components/coreshop-page/coreshop-notice.vue'
    import coreshopcoupon from '@/components/coreshop-page/coreshop-coupon.vue'
    import coreshopblank from '@/components/coreshop-page/coreshop-blank.vue'
    import coreshoptextarea from '@/components/coreshop-page/coreshop-textarea.vue'
    import coreshopvideo from '@/components/coreshop-page/coreshop-video.vue'
    import coreshopimgWindow from '@/components/coreshop-page/coreshop-imgWindow.vue'
    import coreshopimgSingle from '@/components/coreshop-page/coreshop-imgSingle.vue'
    import coreshopgoods from '@/components/coreshop-page/coreshop-goods.vue'
    import coreshoparticle from '@/components/coreshop-page/coreshop-article.vue'
    import coreshoparticleClassify from '@/components/coreshop-page/coreshop-articleClassify.vue'
    import coreshopnavBar from '@/components/coreshop-page/coreshop-navBar.vue'
    import coreshopgroupPurchase from '@/components/coreshop-page/coreshop-groupPurchase.vue'
    import coreshoprecord from '@/components/coreshop-page/coreshop-record.vue'
    import coreshoppinTuan from '@/components/coreshop-page/coreshop-pinTuan.vue'
    import coreshopservice from '@/components/coreshop-page/coreshop-service.vue'
    import coreshoptabbar from '@/components/coreshop-page/coreshop-tabbar.vue'
    import coreshopadpop from '@/components/coreshop-page/coreshop-adpop.vue'
    import coreshopContent from '@/components/coreshop-page/coreshop-content.vue'

    export default {
        name: 'coreshopPage',
        components: {
            coreshopimgSlide,
            coreshopsearch,
            coreshopnotice,
            coreshopcoupon,
            coreshopblank,
            coreshoptextarea,
            coreshopvideo,
            coreshopimgWindow,
            coreshopimgSingle,
            coreshopgoods,
            coreshoparticle,
            coreshoparticleClassify,
            coreshopnavBar,
            coreshopgroupPurchase,
            coreshoprecord,
            coreshoppinTuan,
            coreshopservice,
            coreshoptabbar,
            coreshopadpop,
            coreshopContent
        },
        props: {
            coreshopdata: {
                default: function () {
                    return []
                }
            }
        }
    }
</script>
