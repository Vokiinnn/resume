<template>
    <div class="box">
      <div v-html="contentText" class="resume"></div>
      <div v-html="sucessStyle"></div>
      <div class='countDown'>{{num}}</div>
    </div>
</template>
<script>
export default {
    data(){
        return {
            num:'6'
       }
    },
    props:['contentStyle','contentText'],
    created(){
        this.countDown()
    },
    methods:{
        countDown(){
            let count = function(){
                if( this.num > 0){
                    this.num = this.num - 1
                    console.log(this.num)
                    setTimeout(count,1000)
                }
            }.bind(this)
            count()
        }
    },
    computed:{
        sucessStyle(){
            return '<style>'+ this.contentStyle[0]+this.contentStyle[1] +'</style>'
        }
    }
}
</script>
<style scoped>
.box{
    width:800px;
    margin:auto;
}
.resume{
    width:900px;
    margin:20px auto;
}
.countDown{
    position:absolute;
    font-size:30px;
    right:8%;
    top:30%;
    color:red;
}
</style>