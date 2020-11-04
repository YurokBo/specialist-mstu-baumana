<template>
    <ul class="course__list">
        <li class="course__item" v-for="course in courses" :key="course">
            <a href="#" class="course__link " :class=course.modify>
                <img :src=course.icon :alt=course.name class="course__icon">
                {{course.name}}
            </a>
        </li>
    </ul>
</template>

<script>
    export default {
        name: "Courses",

        data() {
            return {
                courses: [
                    {name: 'программирование, субд, devops', modify: 'light-blue', icon: require('@/assets/img/programming-mobile.png')},
                    {name: 'бизнес-аналитика и excel', modify: 'green', icon: require('@/assets/img/ba-excel-mobile.png')},
                    {name: 'Экономика, менеджмент, реклама, проекты', modify: 'violet', icon: require('@/assets/img/managment-mobile.png')},
                    {name: 'Компьютерная графика, 3D, анимация, САПР', modify: 'mint', icon: require('@/assets/img/graphic-mobile.png')},
                    {name: 'Инфрмационная безопасность, этичный хакинг', modify: 'blue', icon: require('@/assets/img/security-mobile.png')},
                    {name: 'Data Science, Machine Learning, Анализ данных', modify: 'grey-green', icon: require('@/assets/img/data_science-mobile.png')},
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import "Courses";
</style>