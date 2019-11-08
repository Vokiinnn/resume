<template>
  <div class="home" > 
    <v-resume v-if="resumeControl" :contentText="fillContent" :contentStyle="fillStyle" ></v-resume>
    <v-code :code="currentStyle" v-if="styleControl"  ref="styleEditor">
      {{currentStyle}}
    </v-code>
    <v-content v-if="contentControl" :enablehtml="contentControl" :markdown="currenContent" ref="resumeEditor"></v-content>
    <v-controlspeed @sendSpeed="getSpeed"></v-controlspeed>
  </div>
</template>

<script>
import Controlspeed from './Controlspeed'
import Resume from './Resume'
import Code from './Code'
import Content from './Content'
export default {
  name: 'home',
  components:{
    'v-content':Content,
    'v-code':Code,
    'v-resume':Resume,
    'v-controlspeed':Controlspeed
  },
  data () {
    return {
      resumeControl:true,
      styleControl:false,
      contentControl:false,
<<<<<<< HEAD
      speed:'50',
=======
      speed:'100',
>>>>>>> 3b2e9aaf6c98d4a4ec2650194ba1e9b28bd1fbc1
      currentStyle:'',
      fillStyle:[
// 开头设置过渡和背景
`
/*
*首先，自我介绍一下，我叫庄孝杰
*这是我制作的个人简历
*来简单的介绍一下我自己
*但是事先声明哦！没有美工！*_*
*硬伤...
*/
/*先给所有元素加上过渡效果吧*/
*{
  -webkit-transition:all .3s;
  transition:all .3s;
}
/*清除一下默认样式*/
*{
    list-style:none;
    text-decoration:none;
}
/*
*来个背景
*来点音乐...
*开玩笑的...
*/
html{
<<<<<<< HEAD
=======
  background-color:skyblue;
>>>>>>> 3b2e9aaf6c98d4a4ec2650194ba1e9b28bd1fbc1
  color:#222;
  perspective: 600px;
}
.code{
<<<<<<< HEAD
=======
  background-color:skyblue;
>>>>>>> 3b2e9aaf6c98d4a4ec2650194ba1e9b28bd1fbc1
  width:480px;
  min-height:580;
  max-height:580px;
  font-size:1.2rem;
<<<<<<< HEAD
  margin:80px 40px 0 80px;
=======
  margin:40px 0 0 80px;
>>>>>>> 3b2e9aaf6c98d4a4ec2650194ba1e9b28bd1fbc1
  padding:8px;
  overflow-x: hidden;
  overflow-y: auto;
  border:1px solid #000;
  transform: rotate3d(0, 1, 0, 8deg);
}
`
,
//和右边内容同步，显示简历的样式
`
/*
*是不是很难看，一摞一摞的
*来样式~
*/
.resume{
    margin-bottom:50px;
    height:100%;
}
.content{
<<<<<<< HEAD
    width:54%;
    height:100%;
    padding:8px;
    position:relative;
    margin:20px 40px;
=======
    width:60%;
    height:100%;
    padding:8px;
    position:relative;
    background-color:white;
    margin:0 40px 0 40px;
>>>>>>> 3b2e9aaf6c98d4a4ec2650194ba1e9b28bd1fbc1
    right:0;
}
.background{
    border-right:none;
    padding:4px;
    margin-left:8px;
    padding-left:18px;
    position: relative;
    font-size:20px;
    font-weight:999;
}
.background::before{
    content:'';
    position:absolute;
    width:12px;
    height:12px;
    border-radius:50%;
    color:black;
    background-color:black;
    left:-4px;
    top:12px;
}
.project_experience,.profile,.work{
    line-height:38px;
}
<<<<<<< HEAD
.info{
  width:56%;
}
.education{
  width:70%;
}
.info,.education{
    display:flex;
    flex-wrap:wrap;
    line-height:50px;
    justify-content:space-between;
}


=======
.info,.education{
    display:flex;
    line-height:50px;
    justify-content:space-between;
}
>>>>>>> 3b2e9aaf6c98d4a4ec2650194ba1e9b28bd1fbc1
   `
      ],
      currenContent:``,
      fillContent:`
<div class="resume">
        <div class="background">基本信息</div>
        <ul class="info">
            <li>姓名：庄孝杰</li>
<<<<<<< HEAD
            <li>手机号码：13071506018</li>
=======
            <li>手机号码：15992443625</li>
>>>>>>> 3b2e9aaf6c98d4a4ec2650194ba1e9b28bd1fbc1
            <li>出生年月：1997-07</li>
            <li>邮箱：wokiinnn@gmail.com</li>
        </ul>
        <div class="background">教育背景</div>
        <ul class="education">
            <li>2016.09-2019.06</li>
            <li>华立科技职业学院</li>
            <li>软件技术</li>
            <li>大专</li>
        </ul>
        <div class="background">工作经历</div>
        <ul class="work">   
            <li>2018年6月-2019年7月                   广东南方数码科技有限公司</li>
            <li>主要工作：</li>
            <li>1.切图，实现页面效果，JS交互</li>
            <li>2.采用前后端分离开发模式开发项目。</li>
            <li>3.使用Vue全家桶、第三方ui库构建项目</li>
            <li>4.用sass进行代码的编写，运用webpack进行代码的整理和压缩。</li>
            <li>5.Axios与后台交互，合理使用钩子函数实现页面的监听渲染、页面节点实例化功能。</li>
        </ul>
        <div class="background">项目经验</div>
        <ul class="project_experience">
<<<<<<< HEAD
            <li>个人简历</li>
=======
            <li><a href="#">个人简历</a></li>
>>>>>>> 3b2e9aaf6c98d4a4ec2650194ba1e9b28bd1fbc1
        </ul>
        <div class="background">自我评价</div>
        <ul class="profile">
            <li>熟练使用vue、jquery、bootstrap、webpack、git，与es6语法</li>
            <li>学习能力强，有极强的团队合作精神，并且认真负责，有一定的经验去解决问题。</li>
        </ul>
    </div> 
`
    }
  },
  /*
  
  */
  created(){
     this.show()
    //  this.showStyle()
  },
  methods:{
    async show(){
    await this.showResume()
    await this.showStyle(0)
    await this.makeResume()
    await this.showStyle(1)

    },
    test(){
      return new Promise((resolve,reject) => {
        setTimeout(() => {
          console.log(111)
        },10000)
      })
    },
    //获取controlspeed组件的传的值
    getSpeed(data){
        this.speed = data
    },
    //渐进展示简历
    makeResume(){
      return new Promise((resolve,reject) => {
        let show = function(){
          this.contentControl = true
          let contentLength = this.fillContent.length
          if(this.currenContent.length < contentLength){
            this.currenContent = this.fillContent.substring(0,this.currenContent.length + 1)
            let preConLength = this.currenContent[this.currenContent.length -2]
            setTimeout(show,this.speed)
          }else{
            resolve()
          }
        }.bind(this)
        show()
      })
    },
    // 展示代码
    showStyle(n){
      return new Promise((resolve,reject) => {
        let show = (async function(){
          this.styleControl = true
          let style = this.fillStyle[n]
          console.log(style)
          let x = 0
          if(!style){ return  }
          //计算前n个style的字符数
          let length = this.fillStyle.filter((_,index) => index <= n).map(item => item.length).reduce((p,c) => p + c , 0)
          let preStyLength = length - style.length
          if(this.currentStyle.length < length){
            let l = this.currentStyle.length - preStyLength
            let char = style.substring(l, l + 1) || ''
            this.currentStyle += char
            if(style.substring(l - 1 ,l) === '\n' && this.$refs.styleEditor){
              this.$nextTick(() => {
                this.$refs.styleEditor.goBottom()
              })
            }
            setTimeout(show,this.speed)
          }else{
            resolve()
          }
        }).bind(this)
        show()
      })
    },

    //第一阶段直接展示简历，几秒后消失

    showResume(){
      return new Promise((resolve,reject) => {
        setTimeout(() => {
          resolve()
          this.resumeControl = false
          this.styleControl = true
        },6000)
      })
    }
  }
}
</script>

<style scoped >
.home{
  display:flex;
  justify-content:space-between;
<<<<<<< HEAD
  background-image: url('../assets/timg.jpg');
  background-size:100% 110%;
}
.home{
  height:110vh;
=======
>>>>>>> 3b2e9aaf6c98d4a4ec2650194ba1e9b28bd1fbc1
}
</style>
