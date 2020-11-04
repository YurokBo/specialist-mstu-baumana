<template>

    <div class="form__box">
        <form class="form">
            <label for="search" class="form__label">Название курса</label>
            <div class="form__content">
                <input class="form__input" type="text" id="search" :placeholder=placeholderText>
                <button class="form__btn" type="submit">Найти курс</button>
            </div>
        </form>
    </div>

</template>

<script>
    export default {
        name: "Form",

        data() {
            return {
                placeholderText: '',
                width: null
            }
        },

        methods: {
            placeholderChange() {
                this.width = window.matchMedia('(max-width: 768px)').matches
                return this.width ?
                    this.placeholderText = 'Начните поиск...' :
                    this.placeholderText = 'Введите ключевое слово / фразу'
            },
        },

        mounted() {
            //window.addEventListener('resize', this.placeholderChange)
            this.placeholderChange()
        },
        beforeUnmount() {

        },

        unmounted() {
            delete this.placeholderChange()
            alert('Hello')
        },


    }
</script>

<style lang="scss" scoped>
    @import "Form";
</style>