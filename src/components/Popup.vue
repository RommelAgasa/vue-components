<template>
    <div>
        <h2>This is a popup component</h2>
        <input type="text" v-model="name">
        <button @click="$emit('closePopup', name)">Close popup</button>
    </div>
</template>

<script>
    export default {
        name: 'PopupComponent',
        // emits: ['closePopup'],
        emits: {
            closePopup: (name) => {
                if (!name) {
                    console.warn('Name is required to close the popup');
                    return false;
                }
                return true;
            }
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