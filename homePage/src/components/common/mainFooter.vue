<template>
    <div>
        <el-container class="footer-content">
            <el-header height='400' class="header-top">
                  <el-row>
                      <el-col :span='7'>
                          <div class="contact">
                             <div class="contact-title">
                                 <ul>
                                     <li>发送消息 &nbsp ___</li>
                                     <li><el-input class="inp" type="text" placeholder="你的名字" v-model="advices.name"></el-input></li>
                                     <li><el-input class="inp" type="text" placeholder="邮箱地址" v-model="advices.email"></el-input></li>
                                     <li><el-input class="inp" type="text" placeholder="你的电话" v-model="advices.phone"></el-input></li>
                                     <li><el-button type="text" class="but-bg" @click="createCustomer()"><span>在线发送</span>
                                         <img src="http://pbs51uiv3.bkt.clouddn.com/iocn_Shape%205@2x.png"></img>
                                     </el-button></li>
                                     <!-- 消息提醒 -->
                                 </ul>
                             </div>  
                          </div>
                      </el-col>
                      <el-col :span='7'>
                          <div class="method">
                              <ul>
                                  <li> 
                                      <img src="http://pbs51uiv3.bkt.clouddn.com/logo_bslogo@2x.png">
                                  </li>
                                  <li>Phone:0772-2999255</li>
                                  <li>E-mail:carlife52@163.com</li>
                                  <li>Address:柳州市温州商贸城一区3A-1</li>
                              </ul>
                          </div>
                      </el-col>
                      <el-col :span='5'>
                          <div class="navigation">
                              <ul>
                                  <li id="nav">页面导航</li>
                                  <li>首页</li>
                                  <li>关于我们</li>
                                  <li>服务项目</li>
                                  <li>客户案例</li>
                                  <li>新闻资讯</li>
                                  <li>联系我们</li>
                              </ul>
                          </div>
                      </el-col>
                      <el-col :span='5'>
                          <div class="follow">
                              <ul>
                                  <li>关注公众号</li>
                                  <li><img src="http://pbs51uiv3.bkt.clouddn.com/pic_xcx@3x.png" alt="公众号二维码"></li>
                              </ul>
                          </div>
                      </el-col>
                  </el-row>
            </el-header>
            <el-footer height='100' class="footer-bottom">
                  <el-row>
                      <el-col :span='12'>
                          ©备案号:桂Icp备17003197号
                      </el-col> 
                      <el-col :span='12'>
                          <i class="icon iconfont icon-qie"></i>
                          <i class="icon iconfont icon-birdxiaoniao"></i>
                          <i class="icon iconfont icon-kongjian"></i>
                          <i class="icon iconfont icon-weibo"> </i>
                          <i class="icon iconfont icon-pengyouquan"> </i>
                      </el-col>
                  </el-row>
            </el-footer >
        </el-container>
    </div>
</template>
<script>
export default {
    data(){
        return{
            apiUrl: 'http://appwap.52carlife.com/advice',
            advices:{
                name:'',
                email:'',
                phone:''
            }
        }
    },
    methods:{
        createCustomer: function() {
            var vm = this;
            // var advice = JSON.stringify(vm.advices); // 这里是表单数据
            // console.log(advice);
            // 号码验证
            var pattern=/^((13[0-9])|(15[1-3,5-9])|(17[7])|(18[0-9]))\d{8}$/
            var strPhone=pattern.test(vm.advices.phone);
            // 邮箱验证
            var pattern= /^([a-zA-Z0-9]+[_|\_|\.]?)*[a-zA-Z0-9]+@([a-zA-Z0-9]+[_|\_|\.]?)*[a-zA-Z0-9]+\.[a-zA-Z]{2,3}$/;
            var strEmail=pattern.test(vm.advices.email);
             if (vm.advices.name == '' && vm.advices.email=="" && vm.advices.phone == '' ) {
                  this.$message({ 
                       message: '名字不能为空！',
                       type: 'warning',
                       center: true
                    });
                }
                 else if (!strPhone) {
                     this.$message({ 
                       message: '号码格式不对',
                       type: 'warning',
                       center: true
                    });
                 }else if(!strEmail){
                     this.$message({ 
                       message: '邮箱格式不对',
                       type: 'warning',
                       center: true
                    });
                 }       
           else{
            vm.$http.post(vm.apiUrl,vm.advices,{emulateJSON:true}).then((response) => {
                // 是否传值成功
                 console.log(decodeURI(response.data));
                 console.log(decodeURI(response.body));
                //  传值状态
                 console.log(response.status);
                 console.log( response.statusText);

                 console.log( response.headers.get('Expires'));
                
                  this.$message({
                       message: '恭喜你！提交成功！',
                       type: 'success',
                       center: true
            });
            }, (response) => {
                console.log("服务器异常");
            });
        }
        }
    }
}
</script>
<style>
*{
    list-style: none;
    /* text-align: center; */
}
/* @media screen and (max-width: 1200px){   
} */
.footer-content{
    width: 100%;
    background-color: #409EFF;
    color: #fff;
}
.header-top{
    padding: 0 1%;
}
.footer-content .contact{
    height: 18.8vw;
}
.contact /deep/ .el-button{
    color: #fff;
    margin-top: 5px;
}
 .inp{
    border: 0 none;
    border-bottom: 1px solid #fff;
    border-radius: 0px;
}
.contact .el-input__inner{
    width: 14vw;
    margin-top: 0.5vw;
    border-top-width: 0px;
    border-left-width: 0px;
    border-right-width: 0px;
    border-bottom-width: 0px; 
    background:rgba(243, 241, 241, 0);
    color: #fff;
}
.contact .el-input {
    font-size: 0.9vw;
    display: inline-block;
    width: 13vw;
    height: 3vw;
}
 .contact .el-input__inner::-webkit-input-placeholder{
            color:white;
        }
        input::-moz-placeholder{  
            color:white;
        }
        input:-moz-placeholder{    
            color:white;
        }
        input:-ms-input-placeholder{  
            color:white;
        }
.contact .but-bg{
    margin-top: 6%;
    width: 14vw;
    background-image: url(http://pbs51uiv3.bkt.clouddn.com/bg_fsk@2x.png);
    background-repeat: no-repeat;
    background-size: 97% 99%;
}
.contact .but-bg span{
    font-size: 0.2vw;
}
.contact .but-bg img{
    padding-left: 56%;
    width: 0.4vw;
}
.contact .contact-title{
    float: left;
    padding-top: 20px;
    padding-left: 22%;
    width: 77%;
}
.footer-content .method{
    min-height: 18.8vw;
    height: auto;
}
.method ul{
    height: auto;
    margin-top: 0px;
    padding-top: 50px;
    padding-left: 15%;
}
.method img{
    height: auto;
    width: 30%;
    padding-bottom: 10px;
}
.method li{
    line-height: 3vw;
    font-size: 1vw;
}
.footer-content .navigation{
    height: 300px;
}
.navigation ul{
    margin-top: 0px;
    padding-top: 40px;
    padding-left: 30px;
}
.navigation #nav{
    font-size: 1.3vw;
    margin-left: -20px;
}
.navigation ul li{
    line-height: 2vw;
    font-size: 1vw;
}
.footer-content .follow{
    height: 300px;
}
.follow ul{
    margin-top: 0px;
    padding-top: 11%;
    padding-left: 10%;
}
.follow li{
    font-size: 1.2vw;
    line-height: 33px;
}
.follow img{
    width: 6.5vw;
    height: 6.5vw;
    margin-top: 20px;
}
.footer-bottom{
    width: 100%;
    height: 50px;
    background-color: rgb(138, 138, 138);
    padding: 20px 100px;
}
.footer-bottom i{
    padding-right: 20px;
    float: right;
    color: #fff;
    font-size: 1vw;
}
</style>
<style scoped>
 .inp{
        border: 0 none;
        border-bottom: 1px solid #ccc;
        border-radius: 0px;
 }
</style>
