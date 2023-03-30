<template>
    <div class="filter-page">
        <div class="filters">
            <div>
                <span class="filters_span">Тип документа</span>
                <v-select class="filters_item" :input="filter()" :options="types" v-model="selected_type"
                          :reduce="title => title.id"
                          label="title" placeholder="Не выбрано"></v-select>
            </div>
            <div>
                <span class="filters_span">Статус</span>
                <v-select class="filters_item" :input="filter()" :options="status" v-model="selected_status"
                          :reduce="title => title.id"
                          label="title" placeholder="Не выбрано"></v-select>
            </div>
            <div>
                <span class="filters_span">Дате</span>
                <vue-date-picker class="filters_item" @internal-model-change="filter()"
                                 placeholder="Дате" auto-apply format="dd.MM.yyyy"
                                 v-model="select_date" :enable-time-picker="false"></vue-date-picker>
            </div>
        </div>
        <div class="add-elem">добавить документ</div>
    </div>
</template>

<script>
import VSelect from "vue-select";
import VueDatePicker from '@vuepic/vue-datepicker';
import 'vue-select/dist/vue-select.css';
import '@vuepic/vue-datepicker/dist/main.css'

export default {
    name: "FilterPage",
    components: {
        VSelect,
        VueDatePicker
    },
    data() {
        return {
            types: [
                {
                    id: 1,
                    title: 'Договор'
                },
                {
                    id: 2,
                    title: 'Анкета'
                },
                {
                    id: 3,
                    title: 'Справка'
                }
            ],
            status: [
                {
                    id: 1,
                    title: 'Заключен'
                },
                {
                    id: 2,
                    title: 'Расторгнут'
                }
            ],
            select_date: null,
            selected_type: null,
            selected_status: null,
        }
    },
    computed: {
        filter_date() {
            return {
                type: this.selected_type ? this.types.filter(item => item.id === this.selected_type)[0].title : null,
                status: this.selected_status ? this.status.filter(item => item.id === this.selected_status)[0].title : null,
                date: this.select_date
            }
        }
    },
    methods: {
        filter() {
            this.$emit("filter", this.filter_date)
        }
    }
}
</script>

<style lang="scss" scoped>
.filter-page {
    display         : flex;
    align-items     : flex-end;
    justify-content : space-between;
    margin-top      : 90px;
}

.filters {
    display         : flex;
    align-items     : center;
    width           : calc(100% - 250px);
    justify-content : space-between;
    max-width       : 750px;

    &_span {
        font-size     : 14px;
        line-height   : 17px;
        color         : #86939C;
        display       : flex;
        margin-bottom : 5px;
    }

    &_item {
        width        : 160px;
        margin-right : 30px;
    }
}

.add-elem {
    font-weight      : 800;
    font-size        : 16px;
    line-height      : 19px;
    text-align       : center;
    text-transform   : uppercase;
    padding          : 17px 30px;
    background-color : #ffbd27;
    color            : #ffffff;
    border-radius    : 10px;
}
</style>