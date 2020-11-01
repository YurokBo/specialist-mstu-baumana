<template>
    <section class="content">
        <div class="container">
            <Courses/>
            <Form />
        </div>
    </section>
</template>

<script>
    import Courses from "./Courses/Courses";
    import Form from "./Form/Form";

    export default {
        name: "Content",
        components: {Form, Courses}
    }
</script>

<style lang="scss" scoped>

    .content {
        padding: 16px 0 23px;
    }

</style>