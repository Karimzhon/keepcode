<template>
    <div class="app">
        <sidebar></sidebar>
        <div class="content">
            <header>
                <header-page></header-page>
            </header>
            <div class="main">
                <user-card></user-card>
            </div>
        </div>
    </div>
</template>

<script>
import Sidebar from './components/Sidebar.vue';
import HeaderPage from './components/HeaderPage.vue';
import UserCard from './components/UserCard.vue';
export default {
    name: 'App',
    components: {
        Sidebar,
        HeaderPage,
        UserCard,
    }
}
</script>

<style lang="scss" scoped>
.app {
    display  : flex;
    position : relative;
}

.main {
    background-color : #f2f5f8;
    padding : 26px 90px;
    width : 100%;
    min-height : calc(100% - 72px);
}

.content {
    width : calc(100% - 138px);
}

@media (min-width : 1024px) {}

</style>
