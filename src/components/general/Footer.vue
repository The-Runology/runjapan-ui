<template>
    <footer class="bg-white">
        <img src="@/assets/favicon_512.png" alt="logo" height="32" width="32">
        <span class="madewith">
            「<b class="text-danger fw-bold fs-4">潤</b>」
            の決心で作ってきた。
        </span>
        <br>
        <span class="copyright">
            ©2023 
            <a href="/" class="text-decoration-none text-dark">runjp.run</a>
             All rights reserved.</span>
        <br>
        <div class="info-left d-inline-block w-50 text-start ps-4">
            
        </div>
        <div class="info-right d-inline-block w-50">

        </div>
    </footer>
</template>

<script lang="ts">
export default {
    
}
</script>

<style scoped>
footer {
    height: 100px;
    text-align: center;
}
footer .madewith {
    font-family: 'Noto Serif JP', serif;
}
footer .copyright {
    font-family: 'Roman Times';
}

footer .info-left, footer .info-right {
    font-family: 'Noto Serif TC', 'Noto Serif JP', serif;
}

</style>