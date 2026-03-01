<template>
    <div>
        <h2>Custom v-model component</h2>
        <InputElementComponent v-model="name"/>
        <p>Name: {{ name }}</p>
    </div>
</template>

<script>

    import InputElementComponent from './Input.vue';
    export default {
        name: 'VModelCustomComponents',
        components: {
            InputElementComponent
        },
        data() {
            return {
                name: ''
            }
        }
    }
</script>

<style scoped>

</style>