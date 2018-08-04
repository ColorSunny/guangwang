<template>
    <!-- 图片部分 -->
            <div class="first-bottom">
                <el-row>
                        <el-col :span="9.5">
                            <div class="first-bottom-left">
                                <img src="http://pbs51uiv3.bkt.clouddn.com/bj_gs2@2x.png">
                            </div>
                        </el-col>
                        <el-col :span="14.5" class="first-bottom-right-bg">
                            <div class="first-bottom-right">
                                <img src="http://pbs51uiv3.bkt.clouddn.com/bj_gs1@2x.png">
                            </div>
                            <div class="first-bottom-right1">
                                   <div class="content"> 
                                                       &nbsp &nbsp &nbsp {{contentDes}}<br/>
                                                       &nbsp &nbsp &nbsp {{contentCon}}
                                   </div>   
                            </div>
                        </el-col>
                </el-row>
            </div>
</template>
<script>

export default {
    data(){
        return{
            contentDes:' 广西卡莱网络科技有限公司，成立于2017年1月，是一家大数据时代背景下新诞生的典型的互联网+企业， 公司以互联网为依托，深度开发汽车后市场。',
            contentCon:'卡莱科技在成立之初，就深刻认识到时代趋势，决定以互联网为依托，建立让汽车开进互联网的技术平台，我们的着眼点是未来智慧型城市建设，我们将以互联网为技术手段，为智慧型城市的智慧交通提供解决方案。'
        }
    }
}
</script>
<style>
@media (max-width:1590px)  {
    /* --如果浏览器宽度小于1600px */
    body .first-bottom{
       width: 79%;
       margin-left: -1%;
    }
     }
@media (max-width:1400px){
    /* --如果浏览器小于1400px  */
    body .first-bottom{
       width: 93%;
       margin-left: -8%;
    }
    }
@media (max-width: 1200px){
    /* --如果浏览器小于1200px  */
    body .first-bottom{
    width: 102%;
    margin-left: -12%;
}
}
@media (max-width: 1200px){
    /* --如果浏览器小于1200px  */
    body .first-bottom{
    width: 107%;
    margin-left: -18%;
}
}
.first-bottom{
    width: 72%;
    min-height: 350px;
    height: auto;
    padding: 100px 15%;
    margin-left: 1%;
}
.first-bottom-left {
    width: 100%;
}
.first-bottom-left img{
    width: 100%;
    min-height: 509px;
    /* width: auto; */
    height: auto;
    float: right;
    margin-right: -24px;
    margin-top: -4px;
}
.first-bottom-right-bg{
    background-image: url(http://pbs51uiv3.bkt.clouddn.com/bj_jjhsbj@2x.png);
    background-repeat: no-repeat;
    background-size: 100% 100%;
    float: left;
}
.first-bottom-right{
    width: 100%;
    min-height: 200px;
    height: auto;
    text-align: center;
}
.first-bottom-right img{
    max-width: 100%;
    width:auto;
    min-height: 200px;
    height: auto;
}
.first-bottom-right1{
    max-width: 650px;
    width: auto;
    min-height: 300px;
    height: auto;
}
.first-bottom-right1 .content{
    padding:78px 35px;
    line-height: 30px;  
}
</style>
