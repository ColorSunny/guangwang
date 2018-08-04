<template>
<div>
    <!-- 图标联系电话 -->
    <div class="index-header">
        <el-row>
            <el-col :span="12" class="header-img">
                <div>
                  <img src="http://pbs51uiv3.bkt.clouddn.com/logo_logo@2x.png">
                </div>
            </el-col>
            <el-col :span="12">
                <div class="header-phone">
                    <i class="icon iconfont icon-dianhua-copy-copy"></i>
                </div>
                <div class="header-number">
                    <span>
                        {{Hotline}}
                        <span class='phone-number'>{{HotlinePhone}}</span>
                    </span>
                </div>
            </el-col>
        </el-row>
    </div>
<!-- 导航栏 -->
    <div  class="header-nav1">
        <div class="headerNav">
            <el-breadcrumb class='header-nav' separator="|">
                <el-breadcrumb-item></el-breadcrumb-item>
                <el-breadcrumb-item :to="{ path: '/' }" class="el-hover" ><a >{{homePage}}</a></el-breadcrumb-item>
                <el-breadcrumb-item  class="el-hover"><a  @click="aboutUs()">{{aboutUs}}</a></el-breadcrumb-item>
                <el-breadcrumb-item  class="el-hover"><a  @click="serviceProject()">{{serviceProject}}</a></el-breadcrumb-item>
                <el-breadcrumb-item class="el-hover"><a  @click="newsCenter()">{{newsCenter}}</a></el-breadcrumb-item>
                <el-breadcrumb-item class="el-hover"><a @click="serviceCase()">{{serviceCase}}</a></el-breadcrumb-item>
                <el-breadcrumb-item class="el-hover"><a @click="contactUs()">{{contactUs}}</a></el-breadcrumb-item>
                <el-breadcrumb-item></el-breadcrumb-item>     
            </el-breadcrumb>
        </div>        
    </div>
<!-- 大图 -->
    <div class="header-bottom">
        <el-row>
            <el-col :span="14">
                <div class="bottom-left">
                    <pre>{{hiStop}}</pre>
                    <p>{{artifact}}</p>
                    <el-input placeholder="站内搜索" class="input-with">
                        <el-button type="success"  slot="append">{{searchs}}<i class="el-icon-search el-icon--right"></i></el-button>
                    </el-input>
                </div>
            </el-col>
            <el-col :span="10">
                <div class="bottom-right">
                     <img src="http://pbs51uiv3.bkt.clouddn.com/Iphone%20Mockup%20@2x.png"> 
                </div>
            </el-col>
        </el-row>
    </div>
    <!-- 身体部分 -->
    <el-container>
     <el-main>
        <el-container height='2400'>
                    <!-- 第一层 -->
                        <mainFirst></mainFirst>
                    <el-header  height='600'>
                       <!-- 第二层 -->
                      <services></services> 
                    </el-header>
                    <el-main height='600'>
                     <newsCenter></newsCenter>
                    </el-main>
                    <el-footer height='600'>
                      <ServiceCase></ServiceCase>
                    </el-footer>
                  </el-container>
        </el-main>
        <el-footer height='500'>
            <mainFooter></mainFooter>
        </el-footer>          
    </el-container>
</div>
</template>
<script>
import mainFirst from '@/components/common/mainFirst'
import services from '@/components/common/services'
import newsCenter from '@/components/common/newsCenter'
import ServiceCase from '@/components/common/ServiceCase'
import mainFooter from '@/components/common/mainFooter'
export default {
    data(){
        return{
            Hotline:'全国服务热线:',
            HotlinePhone:'0772-2999-255',
            homePage:'卡莱首页',
            aboutUs:'关于我们',
            serviceProject:'服务项目',
            newsCenter:'新闻中心',
            serviceCase:'服务案例',
            contactUs:'联系我们',
            hiStop:'52嗨停',
            artifact:'一款停洗车神器',
            searchs:'搜索'
        }
    },
    components:{
        mainFirst,
        services,
        newsCenter,
        ServiceCase,
        mainFooter,
    },
    mounted () {//给window添加一个滚动滚动监听事件
        window.addEventListener('scroll', this.handleScroll)
    },

    methods:{
        aboutUs:function(){
             $('html, body').animate({scrollTop: 820}, 2000)
             this.showdevIndxNav = true
        },
         serviceProject:function(){
             $('html, body').animate({scrollTop: 1665}, 2000)
             this.showdevIndxNav = true
        },
         newsCenter:function(){
             $('html, body').animate({scrollTop: 2400}, 2000)
             this.showdevIndxNav = true
        },
         serviceCase:function(){
             $('html, body').animate({scrollTop: 3100}, 2500)
             this.showdevIndxNav = true
        },
        contactUs:function(){
            $('html, body').animate({scrollTop: 3500}, 2500)
             this.showdevIndxNav = true
        }
    },
    destroyed () {//离开该页面需要移除这个监听的事件
      window.removeEventListener('scroll', this.handleScroll)
       },
}
</script>
<style>
.el-main{
  overflow: hidden;
}
</style>
<style scoped>
@media screen and (max-width:1590px){ 
   .header-nav1 .header-nav{
    width: 50%;
    padding-left: 25%;
}
}
@media screen and (max-width:1400px){ 
   .header-nav1 .header-nav{
    width: 58%;
    padding-left: 23%;
   }
}
@media screen and (max-width:1200px){ 
   .header-nav1 .header-nav{
    width: 79%;
    padding-left: 18%;
   }
}
@media screen and (max-width:900px){ 
   .header-nav1 .header-nav{
    width: 88%;
    padding-left: 10%;
   }
}
.index-header{
    width: 90%;
    height: 115px;
    background-color: white;
    text-align: center;
    padding: 0 5%;
}
.index-header .el-breadcrumb-item:hover{
    color:red;
}
.index-header .header-img{
    padding: 28px;
}
.index-header .header-phone{
    padding-top: 38px;
    float: left;
    padding-left: 40%;
    color: #409EFF;
}
.header-phone .icon{
    font-size: 32px;
}
.index-header .header-number{
    padding: 30px 10px;
    float: left;
    width: 132px;
}
.header-number .phone-number{
    color: #409EFF;
    font-size: 18px;
}
.header-nav1{
    width: 100%;
    min-height: 32px;
    height: auto;
    text-align: center; 
    clear: both;
    background-color: #409EFF;
}
 .header-nav1 .headerNav{
    width: 100%;
}
.header-nav{
    width: 45%;
    text-align: center; 
    line-height: 2rem;
    color: #fff;
    padding-left: 29%;
    font-size: 0.9vw;
}
.header-nav .el-hover:hover{
    background-image: url(http://pbs51uiv3.bkt.clouddn.com/pic_hsbj@2x.png);
    background-repeat: no-repeat;
    color: #fff;
}
.header-nav a{
    padding: 0 16px;
    color: #fff;
}
.header-bottom{
    height: 640px;
    text-align: center;
    background-image: url(http://pbs51uiv3.bkt.clouddn.com/pic_banner@2x.png);
    background-repeat: no-repeat;
    background-size: 100% 100%;
}
.header-bottom .bottom-left pre{
    font-weight: 500;
    font-size: 50px;
    color: #fff;
    margin-top: 150px;
}
.header-bottom .bottom-left p{
    color: #fff;
}
.bottom-left .input-with{
    padding-top: 100px;
    width: 50%;
}
.bottom-left .input-with .el-button{
    background-color: #409EFF;
    color: #fff;
}
.header-bottom .bottom-right img{
    height: auto;
    margin-top: 55px;
}
</style>
