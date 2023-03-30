<template>
    <div class="app">
        <sidebar></sidebar>
        <div class="content">
            <header>
                <header-page></header-page>
            </header>
            <div class="main">
                <user-card></user-card>
                <filter-page @filter="changeFilter"></filter-page>
                <documents :filter="filter" :key="filter"></documents>
            </div>
        </div>
    </div>
</template>

<script>
import Sidebar from './components/Sidebar.vue';
import HeaderPage from './components/HeaderPage.vue';
import UserCard from './components/UserCard.vue';
import Documents from './components/Documents.vue';
import FilterPage from './components/FilterPage.vue';
export default {
    name: 'App',
    components: {
        Sidebar,
        HeaderPage,
        UserCard,
        Documents,
        FilterPage,
    },
    data() {
        return {
            filter: {
                type: null,
                status: null,
                date: null,
            },
            count: 0
        }
    },
    methods: {
        changeFilter(response) {
            this.filter = response
        }
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

@media (max-width : 1400px) {
    .main {
        padding : 20px 40px;
    }
}

@media (min-width : 1024px) {}

</style>
