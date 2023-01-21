<script lang="ts">
    import IconFavicon from '../icons/IconFavicon.vue';
    import IconSlogan from '../icons/IconSlogan.vue';
    import Button from './Button.vue';
    export default {
        components: { 
            IconFavicon,
            IconSlogan,
            Button
        }
    }

</script>

<template>
    <div id="topbar-container">
        <div class="logo">
            <IconFavicon size="64"></IconFavicon>
            <IconSlogan height="64"></IconSlogan>
        </div>
        
        <Button text="費用計算"></Button>
        <Button text="高才打分"></Button>
        <Button text="簽證介紹"></Button>
    </div>
    
</template>

<style scoped>
    div#topbar-container {
        height: 100px;
        background-color: white;
        display: flex;
        flex-direction: row;
        align-items: center;
    }

    div#topbar-container .logo {
        flex: auto;
    }
</style>