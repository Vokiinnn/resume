<template>
  <div class="code-box" >
    <div class="code" contenteditable="true" ref="container">
      <pre>
        {{code}}
      </pre>
    </div>
    <!-- 加载code模块样式 -->
    <div class="code_style" v-html="addStyle"></div>
  </div>
</template>
<script>
// import Prism from 'prismjs'
export default {
  data() {
    return {
        };
  },
  props:['code'],
  computed:{
    addStyle(){
      return "<style>" + this.code + '</style>'
    }
  },
  methods:{
    goBottom(){
      this.$refs.container.scrollTop = 100000
    }
  } 
};
</script>
<style>
</style>