<template>
    <div class="main3">
        <div class='main3-title'>
             <ul>
                 <li><div id="title-item"></div>INEWS</li>
                 <li><span id="title-i">新闻中心</span>&nbsp &nbsp &nbsp<span>03</span></li>
             </ul>
         </div>
         <div class="main3-content">
             <!-- 两个 -->
             <el-row class="main3-two">
                 <el-col :span='12'>
                     <div class="two-left">
                         <img src="http://pbs51uiv3.bkt.clouddn.com/pic_XWZX@2x.png">
                     </div>
                 </el-col>
                 <el-col :span='12'>
                     <div class="two-right">
                         2018-7-20 &nbsp 05:41:48<br/>
                         <p id="news-title"><a href="#">建立首个无感支付停车场示范</a></p>
                         在柳州本地建设首个无感支付停车场示范点，加快实行构建智慧型城市级停车诱导系统，提高便民
                         <p id="news-more"><i class="icon iconfont icon-changjiantou-copy"></i><a href="#">查看更多</a></p>
                     </div>
                 </el-col>
             </el-row>
             <!-- 三个 -->
             <el-row class="main3-three"  :gutter="50">
                 <el-col :span='8' v-for="(news,index) in newsContents" :key="index">
                     <div class="three-left" :class="{'three-left1':index ==isActive}"  :style="{backgroundImage: 'url(' + (index ==isActive ? news.coverImgUrl : news.baseImg) + ')', backgroundSize:'contain'}" v-on:mouseenter="mouseEnter(index)" v-on:mouseleave="mouseLeave(index)">
                        <div id="left-title">
                            <span id="title1">{{news.newsTitle}}</span><br/>
                            ——
                        </div>
                        <p>&nbsp &nbsp &nbsp &nbsp{{news.newsContent}}</p>
                     </div>
                 </el-col>
             </el-row>
         </div>
    </div>
</template>
<script>
export default {
    data(){
        return{
            isActive:false,
            newsContents:[{
                newsTitle:'如何看待柳州某物业“扣车”收费的行为？',
                newsContent:"14日，一段视频在柳江区拉堡镇柳堡路柳西新城小区居民的朋友圈里疯转，镜头中几名头戴草帽的壮汉将一辆轿车围住，并将轿车车轮锁了起来，车主手持电锯想要拆掉锁头却被阻止，场面火药味十足。物业要求业主缴纳停车费，而业主对物业收取停车费的合理性进行质疑，因而在现场引起了争执。",
                coverImgUrl:'http://pbs51uiv3.bkt.clouddn.com/news333.jpg',
                baseImg:'http://pbs51uiv3.bkt.clouddn.com/baseImg.jpg'
            },
                         {
                newsTitle:'发钱、给奶粉、加产假......你愿意生二孩吗？',
                newsContent:"女性生了孩子，还要负责带孩子，不能参加工作，没有时间去交际，每天的时间就是围着孩子转。当孩子可以上学了，好了，家里人开始催促你出去找工作，去上班了。你才惊恐的发现，你与这个社会脱节了，你已经跟不上社会前进的脚步了，你开始自卑，也就不想改变现状了，这才才是对女性最残忍的地方。",
                coverImgUrl:'http://pbs51uiv3.bkt.clouddn.com/news222.jpg',
                baseImg:'http://pbs51uiv3.bkt.clouddn.com/baseImg.jpg'  
                         },
                         {
                newsTitle:'柳州这所幼儿园，要火！！',
                newsContent:'北京红黄蓝幼儿园虐童事件指：2017年11月22日晚开始，有十余名幼儿家长反映朝阳区管庄红黄蓝幼儿园(新天地分园)国际小二班的幼儿遭遇老师扎针、 喂不明白色药片，并提供孩子身上多个针眼的照片。',
                coverImgUrl:'http://pbs51uiv3.bkt.clouddn.com/news111.jpg',  
                baseImg:'http://pbs51uiv3.bkt.clouddn.com/baseImg.jpg'     
                         }
                         ]
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
    text-decoration: none;
}
.main3-title{
    height: 60px;
    width: 100%;
    margin-top:30px;
}
.main3-title ul{
    float: left;
}
.main3-title ul li{
    width: 230px;
}
.main3-title ul li #title-i{
    font-size: 30px;
    font-weight: bold;
    margin-left: 20px;
}
.main3-title #title-item{
    height: 19px;
    width: 130px;
    background-color:#409EFF;
    float: left;
    margin-right: 20px;
}
.main3-content{
    width: 80%;
    clear: both;
    padding: 30px 10%;
    margin-top: 50px;
    height: 500px;
}
.main3-two{
    width: 90%;
    padding-left: 15%;
}
.main3-two .two-left{
    height: 250px;
    background-color: rgb(119, 115, 115);
}
.two-left img{
    width: 100%;
    height: 100%;
}
.two-right{
    height: 100px;
    padding: 35px 50px;
    color: #000;
}
.two-right #news-title{
    clear: both;
}
.two-right #news-more{
    float: right;
    margin-top: 70px;
}
.two-right #news-more .icon{
    font-size: 50px;
}
.two-right #news-more a{
    position: relative;
    bottom: 14px;

}
.two-right a{
    color: #409EFF;
}
.main3-three{
    margin-top: 30px;
    margin-left: 45px;
}
 .three-left{
    width: 100%;
    min-height: 200px;
    height: auto;
 } 
.three-left #left-title{
    padding-top: 10px;
    padding-left: 20px;
}

.three-left #title1{
    color: #409EFF;
}
 .three-left1{
     color: rgb(14, 13, 13);
 }
 .three-left1 #title1{
     color: #fff;
 }
.main3-three  p{
    font-size: 13px;
}
.three-left p{
    padding: 0 20px;
}
 .three-center{
    width: 100%;
    min-height: 200px;
    height: auto;
    background-color:rgb(219, 214, 214);
 }
 .three-center #left-title{
    padding-top: 10px;
    padding-left: 20px;
}
.three-center p{
    padding: 0 20px;
}
 .three-right{
    width: 100%;
    min-height: 200px;
    height: auto;
    background-color: rgb(219, 214, 214);
 }
 .three-right #left-title{
    padding-top: 10px;
    padding-left: 20px;
}
.three-right p{
    padding: 0 20px;
}
</style>
