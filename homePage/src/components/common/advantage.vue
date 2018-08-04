<template>
        <div class="main-first">
            <!-- 图片部分 -->
            <div class="first2-bottom">
                <el-row>
                        <el-col :span="6">
                            <div class="icon1">
                                <div class="fast">
                                    <div class="icon iconfont icon-pingzi"></div>
                                </div>
                                <ul>
                                    <li id="title"><a href="#">高效快捷</a></li>
                                    <li v-for="item in efficient">{{item.title}}</li>
                                </ul>
                            </div>
                        </el-col>
                        <el-col :span="6">
                            <div class="icon2">
                                <div class="platform">
                                    <div class="icon iconfont icon-zhizhang"></div>
                                </div>
                                <ul>
                                    <li id="title"><a href="#">大数据平台</a></li>
                                    <li v-for="item in bigData">{{item.title}}</li>
                                </ul>
                            </div>
                        </el-col>
                        <el-col :span="6">
                            <div class="icon3">
                                <div class="resource">
                                    <div class="icon iconfont icon-iconset0405"></div>
                                </div>
                                <ul>
                                    <li id="title"><a href="#">整合多方资源</a></li>
                                    <li v-for="item in resources">{{item.title}}</li>
                                </ul>
                            </div>
                        </el-col>
                        <el-col :span="6">
                            <div class="icon4">
                                <div class="service">
                                    <div class='icon iconfont icon-biji'></div>
                                </div>
                                <ul>
                                    <li id="title"><a href="#">专业技术服务</a></li>
                                    <li>Android/Ios</li>
                                    <li>小程序/Html5</li>
                                    <li>平面设计/品牌推广</li>
                                </ul>
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
            efficient:[{title:'目标与价值观'},{title:'团队文化及建设'},{title:'规范标准'}],
            bigData:[{title:'提升业务价值'},{title:'无限的数据潜力'},{title:'机器学习创新'}],
            resources:[{title:'社会资源'},{title:'人力资源'},{title:'财力资源'}],
            services:[{title:'Android/Ios'},{title:'小程序/Html5'},{title:'平面设计/品牌推广'}]
        }
    }
}
</script>
<style scoped>
*{
    list-style: none;
    text-decoration: none;
}
.main-first{
    width: auto;
    background-color: #fff;
    text-align: center;
}
.first2-bottom{
    width: 80%;
    height: 350px;
    text-align: center;
    margin: 12% 10% 12% 10%;
}
.icon1{
    width: 100%;
    height: 100%;
    margin:0;
    padding:0;
    text-align: center;
}
.icon1 .fast{
    width: 100px;
    height: 100px;
    margin-left: 91px;
    background-color: #eee4e4;
    border-radius:50%;
    text-align: center;
}
.fast:hover{
    background-color: rgb(245, 117, 202);
    color: #fff;
}
.icon2 .platform{
    width: 100px;
    height: 100px;
    margin-left: 91px;
    background-color: #eee4e4;
    border-radius:50%;
    text-align: center;
}
.platform:hover{
    background-color: rgb(245, 117, 202);
    color: #fff;
}
.icon3 .resource{
    width: 100px;
    height: 100px;
    margin-left: 91px;
    background-color: #eee4e4;
    border-radius:50%;
    text-align: center;
}
.resource:hover{
    background-color: rgb(245, 117, 202);
    color: #fff;
}
.icon4 .service{
    width: 100px;
    height: 100px;
    margin-left: 91px;
    background-color: #eee4e4;
    border-radius:50%;
    text-align: center;
}
.service:hover{
    background-color: rgb(245, 117, 202);
    color: #fff;
}
.first2-bottom ul{
    margin-top: 45px;
    width: 9vw;
    text-align: center;
    margin-left: 2vw;
}
.first2-bottom ul li{
    line-height: 30px;
}
.first2-bottom ul #title{
    font-size: 18px;
    font-weight: 900;
}
.first2-bottom .icon{
   padding-top: 30px;
   font-size: 32px;
}
.first2-bottom a:hover {
    color: rgb(241, 82, 175);
}
</style>
