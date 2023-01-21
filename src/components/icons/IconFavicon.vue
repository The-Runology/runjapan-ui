<script lang="ts">
    export default {
        props: ['size']
    }
</script>

<template>
    <img src="@/assets/favicon_512.png" :width="size" :height="size" >
</template>