<template>
    <div>
        <h1>Hello {{ name }}, welcome to Vue.js!</h1>
    </div>
</template>

<script>
    export default {
        name: 'GreetUser',
        props: {
            name: {
                type: String,
                required: true
            }
        },
    }
</script>

<style scoped>

</style>

<!-- vbase-css boiler template -->