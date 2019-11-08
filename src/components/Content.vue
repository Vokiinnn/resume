<template>
    <div ref="container" class="content">
        <div v-if="enablehtml"  v-html="markresult"></div>
    </div>
</template>
<script>
import marked from 'marked'
export default {
    data(){
        return {
        }
    },
    props:['markdown','enablehtml'],
    computed:{
        markresult(){
            return this.enablehtml ? marked(this.markdown) : this.markdown
        }
    },
    methods:{
        goBottom(){
            this.$refs.container.scrollTop = 100000
        }
    }
   
}
</script>
<style scoped>
</style>