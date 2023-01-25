<template>
  <Topbar/>
  <Checkbox :options="['自由', '平和']"></Checkbox>
</template>


<script lang="ts">
import Topbar from './components/general/Topbar.vue';
import Checkbox from './components/general/Checkbox.vue';
export default {
  components: {
    Topbar,
    Checkbox
  }
}
</script>


