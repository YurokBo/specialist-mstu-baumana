<template>
    <header class="header">
        <!--<div class="container">-->
            <a :href=createLink(headerBanner.link) class="header__banner" >
                <!--<img :src=headerBanner.img :alt=headerBanner.name class="header__banner-img">-->
            </a>
        <!--</div>-->
    </header>
</template>

<script>
    export default {
        name: "Header",

        data() {
            return {
                headerBanner: {
                    name: 'Скидки на курсы по дипломным программам',
                    img: require('@/assets/img/banner-bg.jpg'),
                    link: 'center?src=new_slider_dp'
                },

            }
        },

        methods: {
            createLink(link) {
                return `https://www.specialist.ru/${link}`
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import "HeaderMobile";
</style>