<template>
    <div>
        <div v-if="data">
            <h3>Name:{{data.name}}</h3>
            <p>{{attemptsFormatted}}</p>
        </div>
        <div v-if="!data">
            please select any data item from list above!
        </div>
    </div>
</template>

<script>
    export default {
        name: "Description",
        props: {
            data: Object
        },
        computed: {
            attemptsFormatted: function() {
                return this.data.attempts + ' Attempts'
            }
        }
    }
</script>

<style scoped>

</style>