<template>
    <div class="main2">
         <div class='main2-title'>
             <ul>
                 <li><div id="title-item"></div>ITEM</li>
                 <li><span id="title-i">{{titleService}}</span>&nbsp &nbsp &nbsp<span>02</span></li>
             </ul>
         </div>
         <div class="main2-content">
             <el-row>
                    <el-col :span="10">
                        <div class="main2-left">
                            <div class="left-title">
                            <h2>{{carLife}}</h2>
                            <span>{{application}}</span>
                            </div>
                            <img src="http://pbs51uiv3.bkt.clouddn.com/pic_xcx@2x.png">
                            <div class="left-content">
                                <p>{{contentFirst}}</p>
                                    <span>{{contentSecond}}</span>   
                            </div>
                        </div>
                    </el-col>
                    <el-col :span="14">
                        <div class="main2-right">
                            <!-- 视频· -->            
                <video width="80%" height="40%" controls>
                        <source src="http://www.runoob.com/try/demo_source/movie.mp4" type="video/mp4">
                        <source src="movie.ogg" type="video/ogg">
                        您的浏览器不支持 HTML5 video 标签。
                </video>
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
            titleService:'服务项目',
            carLife:'52嗨停 应用',
            application:'一款停洗车神器',
            contentFirst:' 以移动互联网为平台，立足柳州，面向全国，网罗全国2亿车主，深度开发汽车后市场O2O模式，为车主提供更便捷，安全智能化的车生活体验。',
            contentSecond:'实时更新空位数量，一键导航、在线预约车位、无感支付、闲置时段车位共享。'
        }
    }
}
</script>
<style scoped>
*{
    list-style: none;
}
.main2-title{
    height: 60px;
    width: 100%;
}
.main2-title ul{
    float: left;
}
.main2-title ul li{
    width: 230px;
}
.main2-title ul li #title-i{
    font-size: 30px;
    font-weight: bold;
    margin-left: 20px;
}
.main2-title #title-item{
    height: 19px;
    width: 130px;
    background-color:#409EFF;
    float: left;
    margin-right: 20px;
}
.main2-content{
    width: 80%;
    clear: both;
    padding: 30px 10%;
    margin-top: 50px;
    height: 500px;
    background-color:#409EFF;
}
.main2-left{
    height: 20vw;
    color: #fff;
}
.main2-left .left-title{
    float: left;
    margin-top:3vw;
    margin-left: 4vw;
}
.main2-left img{
    float: left;
    margin-top: 4vw;
    margin-left: 5vw;
}
.main2-left .left-content{
    clear: both;
    padding: 3vw 1vw;
    line-height: 2vw;
}
.main2-right{
    text-align: center;
}
.main2-right video{
    padding: 1.8vw 0;
}
</style>
