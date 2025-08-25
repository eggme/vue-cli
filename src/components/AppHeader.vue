<template>
    <header>
        <h1>{{ header }}</h1>
        <button v-on:click="sendEvent">send</button>
    </header>
</template>

<script>
export default {
    props: ["header"],
    data: function() {
        return {
            count: 0,
        }
    },
    methods: {
        sendEvent: function() {
            return this.$emit("renew", this.count++)
        }
    }
}
</script>

<style>

</style>