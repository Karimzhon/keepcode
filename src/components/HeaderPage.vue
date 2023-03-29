<template>
    <div class="header">
        <ul class="header-breadcrumb">
            <li class="header-breadcrumb_item">
                Главная
                <span>/</span>
            </li>
            <li class="header-breadcrumb_item">
                Ученики
                <span>/</span>
            </li>
            <li class="header-breadcrumb_item">
                Документы
            </li>
        </ul>
        <div class="header-profile">
            <img src="/src/assets/user.png" alt="" class="user-photo">
            <p class="header-profile_name">
                Name_user
            </p>
            <a href="#" class="settings-logo">
                <img src="/src/assets/settings.svg" alt="settings">
            </a>
            <a href="#" class="logout-logo">
                <img src="/src/assets/logout.svg" alt="settings">
            </a>
        </div>
    </div>
</template>

<script>
export default {
    name: "HeaderPage"
}
</script>

<style lang="scss" scoped>
.header {
    height           : 72px;
    background-color : #ffffff;
    padding          : 16px 90px;
    display          : flex;
    align-items      : center;
    justify-content  : space-between;

    &-profile {
        display     : flex;
        align-items : center;

        .user-photo {
            width         : 40px;
            height        : 40px;
            border-radius : 50%;
            margin-right  : 10px;
        }

        &_name {
            font-size    : 18px;
            line-height  : 22px;
            color        : #0d2839;
            margin-right : 53px;
        }

        .settings-logo {
            margin-right : 33px;
            display      : flex;

            img {
                height : 25px;
                width  : 25px;
            }
        }

        .logout-logo {
            display : flex;

            img {
                height : 25px;
                width  : 25px;
            }
        }
    }

    &-breadcrumb {
        list-style  : none;
        display     : flex;
        align-items : center;

        &_item {
            display     : flex;
            text-shadow : 0 4px 4px rgba(0, 0, 0, 0.25);
            font-weight : 300;
            color       : #0d2839;
            font-size   : 14px;
            line-height : 17px;

            span {
                margin : 0 5px;
            }

            &:last-child {
                color : #86939c;
            }
        }
    }
}
</style>