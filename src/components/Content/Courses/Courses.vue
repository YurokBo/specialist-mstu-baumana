<template>
    <ul class="course__list">
        <li class="course__item" v-for="course in courses" :key="course">
            <a href="#" class="course__link " :class=course.modify>
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
                    {name: 'программирование, субд, devops', modify: 'light-blue'},
                    {name: 'бизнес-аналитика и excel', modify: 'green'},
                    {name: 'Экономика, менеджмент, реклама, проекты', modify: 'violet'},
                    {name: 'Компьютерная графика, 3D, анимация, САПР', modify: 'mint'},
                    {name: 'Инфрмационная безопасность, этичный хакинг', modify: 'blue'},
                    {name: 'Data Science, Machine Learning, Анализ данных', modify: 'grey-green'},
                ]
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import "Courses";
</style>