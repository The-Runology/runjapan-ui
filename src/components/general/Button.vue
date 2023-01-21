<script lang="ts">
    export default {
        props: ['text']
    }
</script>
<template>
    <a>
        <span>
            {{ text }}
        </span>
    </a>
</template>

<style scoped>
    a {
        color: #b80012;
        width: 100px;
        height: 40px;
        display: flex;
    }

    a span {
        display: block;
        margin: auto;
        text-align: center;
    }

    a:hover {
        background-color: #b80012;
        color: white;
        border-radius: 10px;
    }
</style>