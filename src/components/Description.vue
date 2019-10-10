<template>
    <div>
        <div v-if="data">
            <h3>Name:{{data.name}}</h3>
            <p>Attempts: {{data.attempts}}</p>
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
        }
    }
</script>

<style scoped>

</style>