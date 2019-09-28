<template>
  <div id="app">
    <Home/>
  </div>
</template>

<script>
import Home from './components/Home'
export default {
  name: 'App',
  components: {
    Home
  }
}
</script>

<style>
/* #app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
body,div,pre,ul,li{
  margin:0;
  padding:0;
}
#app{
  height:100%;
  width:100%;
  font-size:20px;
}
</style>
