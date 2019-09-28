<template>
    <div class="control">
        <label>速度</label> 
        <select @change="sendSpeed" v-model="value">
            <option :value="item.id" v-for="(item,index) in speeds" :key="index" ref="thisData">{{item.speed}}</option>
        </select>
    </div>
</template>
<script>
export default {
    data(){
        return {
            value:{},
            defaultSpeed:'',
            speeds: [
                {speed:1000,id:0},
                {speed:500,id:1},
                {speed:200,id:2},
                {speed:100,id:3},
                {speed:50,id:4},
                {speed:30,id:5},
                {speed:20,id:6},
                {speed:0,id:7}
            ]
        }
    },
    methods:{
        sendSpeed(){
            this.$emit('sendSpeed',parseInt(this.$refs.thisData[this.value].text))
            // console.log(typeof(parseInt(this.$refs.thisData[this.value].text)))
        }
    },
    activity(){
        this.sendSpeed()
    }
}
</script>
<style>
    .control{
        position:absolute;
        top:2%;
        right:4%;
    }
</style>