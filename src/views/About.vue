<template>
    <div class="about">
        <h1>This is an about page</h1>
        <Calendar
                v-on:choseDay="clickDay"
                v-on:changeMonth="changeDate"
                v-on:isToday="clickToday"
        ></Calendar>
    </div>
</template>
<script>
    import Calendar from 'vue-calendar-component';

    export default {
        data() {
            return {
                /* arr:[
                     {date:'2018/4/1',className:"mark1"}, {date:'2018/4/13',className:"mark2"}
                 ]*/
            }
        },
        components: {
            Calendar
        },
        methods: {
            clickDay(data) {
                console.log(data);
            },//选中某天
            changeDate(data) {
                console.log(data); //左右点击切换月份
            },
            clickToday(data) {
                console.log(data); //跳到了本月
            }

        }
    }

</script>
<style lang="stylus">
    .wh_content_all
        background-color #fff !important

    .wh_jiantou1
        border-top 2px solid #000 !important
        border-left 2px solid #000 !important

    .wh_content_li
    .wh_top_tag
    .wh_item_date
        color #000

    .wh_jiantou2
        border-top 2px solid #000 !important
        border-right 2px solid #000 !important

    .wh_isToday
        background-color #fff !important
        color #0AC5C6

    .wh_chose_day
        background-color #0AC5C6 !important
        color #fff

    .wh_top_changge
     .wh_content_li
        color #000 !important
</style>
