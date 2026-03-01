<template>
    <div>
        <h2>Article Component</h2>
        <h2>{{ title }}</h2>
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
        }
    }
</script>

<style scoped>

</style>