<template>
  <div id="app">

    <app-header/>
    
    <app-main/>

    <app-footer/>
    
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppFooter from './components/AppFooter.vue'

export default {
  name: 'App',
  components: {
    AppHeader,
    AppMain,
    AppFooter
  }
}
</script>

<style lang="scss">
@import './style/variables';
@import './style/general';

ul li{
  cursor: pointer;
}
</style>
