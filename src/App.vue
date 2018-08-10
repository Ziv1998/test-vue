<template>
  <div id="app">
    <AppHeader/>
    <AppMenu/>
  </div>
</template>

<script>
  //import TestView from './components/TestView.vue'
  //import HelloWorld from './components/HelloWorld.vue'
  import AppHeader from './components/header/AppHeader.vue';
  import AppMenu from './components/menu/AppMenu.vue';
  export default {
    name: "app",
    components:{
      AppHeader,
      AppMenu
    }
  }
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  overflow: hidden;
}
</style>
