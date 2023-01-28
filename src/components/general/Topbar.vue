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
            <a href="./">
                <IconFavicon size="64"></IconFavicon>
                <IconSlogan height="64" class="d-none d-md-inline-block"></IconSlogan>
            </a>
        </div>
       
        <Button class="run-btn red" text="費用計算" padding="10px"></Button> 
        <Button class="run-btn red" text="高才打分" padding="10px"></Button>
        <Button class="run-btn red" text="簽證介紹" padding="10px"></Button>
        <Button class="run-btn red" text="潤學の神社" padding="10px"></Button>
    </div>
    
</template>

<style scoped>
    div#topbar-container {
        height: 100px;
        background-color: white;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: space-between;
    }

    div#topbar-container .logo {
        flex: auto;
    }

    @media (max-width: 515px) {
        div#topbar-container {
            height: 150px;
        }

        #topbar-container .run-btn {
            width: 25px;
            height: 100px;
            margin: auto 12px;
        }
    }


</style>