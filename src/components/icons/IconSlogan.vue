<script lang="ts">
    export default {
        props: [
            'width',
            'height'
        ]
    }
</script>

<template>
    <img src="@/assets/slogan.png" :width="width" :height="height"> 
</template>