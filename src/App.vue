<template>
    <Header/>
    <Content />
</template>

<script>

    import Header from "./components/Header/Header";
    import Content from "./components/Content/Content";

    export default {
        name: 'App',
        components: {
            Content,
            Header

        }
    }
</script>

<style lang="scss">
    @import "@/assets/styles/base.scss";
</style>
