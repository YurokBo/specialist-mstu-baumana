<template>
    <section class="header">
        <div class="container">
            <div class="header__banner">
                <a href="https://www.specialist.ru/" class="header__banner-link">
                    <img :src=headerBanner alt="headerBanner" class="header__banner-img">
                </a>
            </div>
        </div>
        <div class="header__courses">
            <div class="container">
                <ul class="header__courses-list">
                    <li class="header__courses-item" v-for="course in headerCourses" :key="course">
                        <a :href=createLink(course.link) class="header__courses-link">
                            <img :src=course.icon :alt=course.name>
                            {{ course.name }}
                        </a>
                    </li>
                </ul>
            </div>
        </div>
        <div class="header__form">
            <div class="container">
                <Form />
            </div>
        </div>
    </section>
</template>

<script>
    import Form from "../Mobile/Content/Form/Form";
    export default {
        name: "HeaderDesctop",
        components: {Form},
        data() {
            return {
                headerBanner: require('@/assets/img/header-decktop-banner.jpg'),

                headerCourses: [
                    {
                        icon: require('@/assets/img/data_science-desk.png'),
                        name: 'Data Science, Machine Learning, Анализ данных',
                        link: 'dictionary/definition/data_science'
                    },
                    {
                        icon: require('@/assets/img/programming-desk.png'),
                        name: 'Программирование, СУБД и DevOps',
                        link: 'section/programming'
                    },
                    {
                        icon: require('@/assets/img/managment-desk.png'),
                        name: 'Экономика, менеджмент, реклама, проекты',
                        link: 'section/management'
                    },
                    {
                        icon: require('@/assets/img/ba-excel-desk.png'),
                        name: 'Бизнес-аналитика и Excel',
                        link: 'section/business-analytics'
                    },
                    {
                        icon: require('@/assets/img/graphic-desk.png'),
                        name: 'Компьютерная графика, 3D, анимация, САПР',
                        link: 'section/design'
                    },
                    {
                        icon: require('@/assets/img/security-desk.png'),
                        name: 'Информационная безопасность, этичный хакинг',
                        link: 'section/information-security'
                    },
                ]
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
    @import "HeaderDesctop";
</style>