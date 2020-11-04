<template>
    <section class="content">
        <div class="container">
            <Courses />
            <Form />
        </div>
    </section>
</template>

<script>
    import Courses from "./Courses/Courses";
    import Form from "./Form/Form";

    export default {
        name: "ContentMobile",
        components: {Form, Courses}
    }
</script>

<style lang="scss" scoped>

    .content {
        display: none;
        padding: 16px 0 23px;
    }

    @media (max-width: 720px) {
        .content {
            display: block;
            padding: 16px 0 23px;
        }
    }

</style>