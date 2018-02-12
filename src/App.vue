<template>
  <div id="app">
    <img src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
    <SocialShare />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import SocialShare from './components/SocialShare.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    SocialShare
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
  margin-top: 60px;
}
</style>
