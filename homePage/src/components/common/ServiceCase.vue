<template>
    <div class="main4">
         <div class='main4-title'>
             <ul>
                 <li><div id="title-item"></div>SERVE</li>
                 <li><span id="title-i">{{titleSer}}</span>&nbsp &nbsp &nbsp<span>04</span></li>
             </ul>
         </div>
         <div class="main4-content">
             <el-row class="content-four">
                 <el-col :span='6'  v-for="(title,index) in titles" class="content-col" :key="index">
                     <div id="content-img">
                          <img :src="title.imgUrl">
                          <div class="img-title" :class="{'img-title1':index ==isActive}" v-on:mouseenter="mouseEnter(index)" v-on:mouseleave="mouseLeave(index)"><div class="d"><div class="d2">{{title.title}}</div></div></div>
                     </div>
                 </el-col>
             </el-row>
         </div>
    </div>
</template>
<script>
export default {
    data () {
    return {
        titleSer:'服务案例',
        isActive:false,
        titles:[{
            title:'商业综合体',
            imgUrl:"http://pbs51uiv3.bkt.clouddn.com/2014113144031635506224314065000@2x.png"
        },
        {
            title:'停车场',
            imgUrl:"http://pbs51uiv3.bkt.clouddn.com/pic_zhcc@2x.png"
        },
        {
            title:'智慧社区',
            imgUrl:"http://pbs51uiv3.bkt.clouddn.com/pic_o20sq@2x.png"
        },
        {
            title:'城市规划',
            imgUrl:"http://pbs51uiv3.bkt.clouddn.com/ff80808136390a8a01373149a50a04d4@2x.png"
        },]
    }
    },
    methods:{
        mouseEnter:function(index){
          this.isActive = index;
        },
         //鼠标移除
       mouseLeave:function(){
            this.isActive = null;  
      },
    }
}
</script>
<style scoped>
*{
    list-style: none;
}
.main4-title{
    height: 60px;
    width: 100%;
    margin-top:30px;
}
.main4-title ul{
    float: left;
}
.main4-title ul li{
    width: 230px;
}
.main4-title ul li #title-i{
    font-size: 30px;
    font-weight: bold;
    margin-left: 20px;
}
.main4-title #title-item{
    height: 19px;
    width: 130px;
    background-color:#409EFF;
    float: left;
    margin-right: 20px;
}
.main4-content{
    text-align: center;
    width: 80%; 
    clear: both; 
    padding: 30px 10%;
    margin-top: 50px;
    height: 500px;
}
.main4-content .content-four{
    width: 90%;
    height: 18.8vw;
    margin: 100px 5%;
    text-align: center;
}
.content-four #content-img img{
    width: 85%;
    height: 18.8vw;
}
.content-four .content-col{
    height: 300px;
}
.content-four #content-img .img-title{
    width: 85%;
    height: 3.2vw;
    background: rgb(20, 20, 20);
    opacity: 0.5;
    margin-top: -20%;
    margin-left: 7.5%;
    text-align: center;
    color: #fff;
}
.img-title .d{
    padding-top: 6%;
}
 .content-four #content-img .img-title1{
    width: 85%;
    height: 18.8vw;
    background: rgb(20, 20, 20);
    opacity: 0.6;
    text-align: center;
    color: #fff;
    margin-top: -19vw;
    margin-left: 7.5%;
    display: flex;
    flex-direction: row;
    align-items: center;
}
.img-title1 .d{
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: row;
    align-items: center;
    
}
.img-title1 .d2{
    width: 100%;
    height: 63px;
    background-image: url(http://pbs51uiv3.bkt.clouddn.com/bg_fsk@2x.png);
    background-repeat: no-repeat;
    background-size: 95% 56%;
    padding-top: 7px;  
    margin-left: 0.56vw;
} 
</style>
