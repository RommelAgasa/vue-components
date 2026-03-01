<template>
    <div>
        <h2>Article Component</h2>
        <h2 v-bind="$attrs">{{ title }}</h2>
        <h2>Likes: {{ likes }}</h2>
        <h2>Published: {{ isPublished ? 'Yes' : 'No' }}</h2>
    </div>
</template>

<script>
    export default {
        name: 'ArticleComponent',
        props: {
            title: String,
            likes: {
                type: Number,
                default: 0
            },
            isPublished: Boolean
        },
        inheritAttrs: false, // This prevents the attributes from being automatically added to the root element of the component
    }
</script>

<style scoped>

</style>