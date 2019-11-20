<template>
    <div class="post-header-container">
        <h1 class="title">{{ title }}</h1>
        <div class="other-info">
            <p class="author">{{ author }}</p>
            <p class="post-time">{{ postTime }}</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: "PostHeader",
        props: ['title', 'postTime', 'author']
    }
</script>

<style scoped>

</style>