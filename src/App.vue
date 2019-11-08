<template>
  <div id="app">
    <Home/>
    <p class="record">粤ICP备19124318号-1</p>
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

body,div,pre,ul,li{
  margin:0;
  padding:0;
}
body{
  height:100%;
  box-sizing: border-box;
}
#app{
  height:100%;
  width:100%;
  font-size:20px;
}
.record{
  margin-bottom:10px;
  text-align:center;
}
</style>
