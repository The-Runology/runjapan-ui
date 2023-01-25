<script lang="ts">
    export default {
        props: {
            text: String,
        }
    }
</script>
<template>
    <button>
        {{ text }}
    </button>
</template>

<style scoped>

    button.run-btn {
        border: none;
        border-radius: 10px;
        width: 100px;
        height: 40px;
        transition: 0.2s all;
    }

    button.run-btn:active {
        transform: scale(0.96);
    }

    button.run-btn.bg-primary {
        background-color: #b80012;
        color: white;
    }

    button.run-btn.primary {
        color: #b80012;
        transition: 0.2s all;
    }

    button.run-btn.primary:hover {
        color: white;
        background-color: #b80012;
    }

    button.run-btn.primary:active {
        color: white;
        background-color: #b80012;
    }

    button.run-btn.bg-pink {
        background-color: #f9dae7;
        color: #c10049;
    }

    button.run-btn.pink {
        color: #c10049;
    }

    button.run-btn.pink:hover {
        background-color: #f9dae7;
        color: #c10049;
    }

</style>