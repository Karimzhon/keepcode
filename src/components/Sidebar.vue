<template>
    <div class="sidebar">
        <div class="sidebar-logo">
            <img src="/src/assets/logo.svg" alt="Logo">
        </div>
        <div class="sidebar-menu">
            <a href="#" class="sidebar-menu_item">
                <img src="/src/assets/home.svg" alt="Home">
                <p class="sidebar-menu_item_text">
                    Главная
                </p>
            </a>
            <a href="#" class="sidebar-menu_item">
                <img src="/src/assets/calendar.svg" alt="Calendar">
                <p class="sidebar-menu_item_text">
                    Расписание
                </p>
            </a>
            <a href="#" class="sidebar-menu_item active">
                <img src="/src/assets/student.svg" alt="Students">
                <p class="sidebar-menu_item_text">
                    Ученики
                </p>
            </a>
            <a href="#" class="sidebar-menu_item">
                <img src="/src/assets/teacher.svg" alt="Teacher">
                <p class="sidebar-menu_item_text">
                    Преподаватели
                </p>
            </a>
            <a href="#" class="sidebar-menu_item">
                <img src="/src/assets/lesson.svg" alt="Lesson">
                <p class="sidebar-menu_item_text">
                    Занятия
                </p>
            </a>
            <a href="#" class="sidebar-menu_item">
                <img src="/src/assets/group.svg" alt="Groups">
                <p class="sidebar-menu_item_text">
                    Группы
                </p>
            </a>
        </div>
    </div>
</template>

<script>
export default {
    name: "Sidebar"
}
</script>

<style lang="scss" scoped>
.sidebar {
    width      : 138px;
    height     : 100vh;
    position   : sticky;
    top        : 0;
    background : #458AFB;
    filter     : drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
    overflow-y : scroll;

    &-logo {
        padding : 15px 22px;
    }

    &-menu {
        display        : flex;
        flex-direction : column;
        align-items    : center;

        &_item {
            width           : 100%;
            text-align      : center;
            text-decoration : none;
            padding         : 20px 0;
            color           : #ffffff;
            font-size       : 18px;
            line-height     : 22px;
            display         : flex;
            flex-direction  : column;
            align-items     : center;

            img {
                margin-bottom : 5px;
            }

            &.active {
                background-color : #5696ff;
            }
        }
    }
}
</style>