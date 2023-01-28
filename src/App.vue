<template>
  <Topbar/>
  <HomeView />
  <Footer />
</template>


<script lang="ts">
import Topbar from './components/general/Topbar.vue';
import Footer from './components/general/Footer.vue';
import HomeView from '@/views/HomeView.vue';
export default {
  components: {
    Topbar,
    Footer,
    HomeView
  }
}
</script>


