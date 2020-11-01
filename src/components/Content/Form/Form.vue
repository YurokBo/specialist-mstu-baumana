<template>

    <div class="form__box">
        <form class="form">

            <label for="search" class="form__label">Название курса</label>
            <div class="form__content">
                <input class="form__input" type="text" id="search" placeholder="Начните поиск...">
                <button class="form__btn" type="button">Найти курс</button>
            </div>
        </form>
    </div>

</template>

<script>
    export default {
        name: "Form"
    }
</script>

<style lang="scss" scoped>
    @import "Form";
</style>