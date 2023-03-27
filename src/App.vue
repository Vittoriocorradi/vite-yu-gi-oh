<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';

export default {
  name: 'Yu-Gi-Oh',
  components: {
    AppHeader,
    AppMain
  }
}
</script>

<template>
  <AppHeader></AppHeader>
  <AppMain></AppMain>
</template>

<style>
  body {
    height: 100vh;
  }

  #app {
    height: 100%;
  }
</style>
