<template>
    <div>
        <h3 v-for="name in names" :key="name.firstName">
            <slot :firstName="name.firstName" :lastName="name.lastName"></slot>
        </h3>
        
    </div>
</template>

<script>
    export default {
        name: 'SlotProps',
        data() {
            return {
                names: [
                    { firstName: 'John', lastName: 'Doe' },
                    { firstName: 'Jane', lastName: 'Smith' },
                    { firstName: 'Alice', lastName: 'Johnson' }
                ]
            }
        }
    }
</script>

<style scoped>

</style>