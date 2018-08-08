<template>
  <div id="app">
    <AppHeader/>
    <AppMenu/>
    <AppContent/>
  </div>
</template>

<script>
  //import TestView from './components/TestView.vue'
  //import HelloWorld from './components/HelloWorld.vue'
  import AppHeader from './components/header/AppHeader.vue';
  import AppMenu from './components/menu/AppMenu.vue';
  import AppContent from './components/content/AppContent.vue';
  export default {
    components:{
      AppHeader,
      AppMenu,
      AppContent
    }
  }
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  overflow: hidden;
}
</style>
