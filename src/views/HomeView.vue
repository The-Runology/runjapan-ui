
<template>
<div class="bg-white bg">
  <div class="button-area d-flex justify-content-evenly">
    <Button class="run-btn bg-red run" text="一鍵跑路🏃" fontSize="35px"></Button>
  </div>
  <div class="suggest d-flex flex-row">
    
  </div>
</div> 
</template>

<script lang="ts">
import Button from '../components/general/Button.vue';
export default {
  components: {
    Button
  }
}
</script>

<style scoped>
div.bg {
  width: 100%;
  height: 1000px;
}

</style>