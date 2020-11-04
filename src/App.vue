<template>
    <HeaderDesktop/>
    <HeaderMobile/>
    <ContentMobile/>
</template>

<script>

    import HeaderMobile from "./components/Mobile/Header/HeaderMobile/HeaderMobile";
    import ContentMobile from "./components/Mobile/Content/ContentMobile";
    import HeaderDesktop from "./components/Desktop/HeaderDesktop";

    export default {
        name: 'App',
        components: {
            HeaderDesktop,
            ContentMobile,
            HeaderMobile

        }
    }
</script>

<style lang="scss">
    @import "@/assets/styles/base.scss";
</style>
