<template>
  <div id="app">
    <MyHeader/>
    <img class="vue_logo" alt="Vue logo" src="./assets/logo.png">

    <h2>Chat Bot</h2>
    
    <MyComponent/>
    <MyFooter/>
  </div>
</template>

<script>

import MyComponent from './components/MyComponent.vue';
import MyHeader from './components/MyHeader.vue';
import MyFooter from './components/MyFooter.vue';

export default {
  name: 'App',
  components: {
    
    MyComponent,
    MyHeader,
    MyFooter
  }
}
</script>

<style lang="scss">
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
  
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #16fe06;
  
  background-color: black;
  
  background-size: cover;
  width: 100%;

  .vue_logo {
    width: 100px;
    height: 100px;
  }
  
}
</style>
