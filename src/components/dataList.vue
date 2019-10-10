<template>
    <div>
        <ul>
            <li v-for="item in items" v-bind:key="item.id" v-on:click="getItem(item)">
                {{item.name}}
            </li>
        </ul>
        <Description v-bind:data="activeItem" />
    </div>
</template>

<script>

    import Description from "@/components/Description";

    export default {
        name: "DataList",
        components: {
           Description
        },
        data: function() {
        return {
            activeItem: {
                id: 0,
                name: '',
                attempts: 0
            },
            items:  [
                {
                    id: "1",
                    name: "abc",
                    attempts: "7"
                },
                {
                    id: "2",
                    name: "bed",
                    attempts: "6"
                },
                {
                    id: "3",
                    name: "efg",
                    attempts: "9"
                },
                {
                    id: "4",
                    name: "hij",
                    attempts: "2"
                }
            ]};
        },
        methods: {
            getItem: function(item) {
                this.activeItem = item;
            }
        }
    }
</script>

<style scoped>

</style>