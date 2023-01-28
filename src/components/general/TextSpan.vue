<template>
    <span class="d-block run-span" :style="{
        fontSize: fontSize + 'px',
        fontFamily: font,
        width: fontSize * 1.4 + 'px',
        padding: padding + 'px'
    }">
        {{  text  }}
    </span>
</template>

<script lang="ts">
export default {
    props: {
        text: String,
        fontSize: {
            type: Number,
            default: 14
        },
        font: {
            type: String,
            default: 'Yuji Syuku'
        },
        width: {
            type: Number,
        },
        padding: {
            type: Number,
            default: 10
        }
    }
}
</script>

<style scoped>
span.run-span.bg-red {
    background-color: #b80012;
    color: white;
}
</style>