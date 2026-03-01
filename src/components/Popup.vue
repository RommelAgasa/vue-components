<template>
    <div>
        <h2>This is a popup component</h2>
        <button @click="$emit('closePopup', 'Kyla')">Close popup</button>
    </div>
</template>

<script>
    export default {
        name: 'PopupComponent',
        emits: ['closePopup']
    }
</script>

<style scoped>

</style>