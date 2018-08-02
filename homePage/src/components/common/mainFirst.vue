<template>
        <div class="main-first">
            <!-- 导航栏 可用v-if-->
            <div class="first-top">
                <div class="first-top-center">
                <div  class="first-top-nav1" :class="{'first-top-nav2':changed == index}"  @click="changeCss(index)" 
                      v-for="(item,index) in items" :key="index" v-on:mouseenter="changedd(index)" v-on:mouseleave="mouseLeave()">
                    <ul>
                        <li> 
                            <img :src="changed == index ? item.url1:item.url">
                        </li>
                        <li id='nav-title'>{{item.title}}</li>
                        <li><hr/></li>
                        <li id="nav-descript">{{item.desc}}</li> 
                    </ul>
                </div>
                </div>
            </div>
            <!-- 四个 -->
            <mainFirst1 v-show="isshow"></mainFirst1>
            <mainFirst2 v-show="isshow1"></mainFirst2>
            <mainFirst3 v-show="isshow2"></mainFirst3>
            <mainFirst4 v-show="isshow3"></mainFirst4> 
        </div>    
</template>
<script>
import { swiper, swiperSlide } from 'vue-awesome-swiper'
import mainFirst1 from '@/components/common/mainFirst1'
import mainFirst2 from '@/components/common/mainFirst2'
import mainFirst3 from '@/components/common/mainFirst3'
import mainFirst4 from '@/components/common/mainFirst4'
export default {
 data () {
    return {
      changed:0,
      isshow:true,
      isshow1:false,
      isshow2:false,
      isshow3:false,
      //图片数据
    items: [{
        url: 'http://pbs51uiv3.bkt.clouddn.com/iocn_logo@2x.png',
        url1:'http://pbs51uiv3.bkt.clouddn.com/pic_logo1@2x1.png',
        title:'公司简介',
        desc: '广西卡莱网络科技有限公司，成立于2017年1月，是一家大数据'
      }, {
        url: 'http://pbs51uiv3.bkt.clouddn.com/iocn_ystd@2x.png',
        url1: 'http://pbs51uiv3.bkt.clouddn.com/like2@2x1.png',
        title:'优势特点',
        desc: '拥有专业的技术团队和规范的管理流程'
      }, {
        url: 'http://pbs51uiv3.bkt.clouddn.com/iocn_td@2x.png',
        url1: 'http://pbs51uiv3.bkt.clouddn.com/iocn_qytd@2x1.png',
        title:'企业团队',
        desc: '完成《城市级停车诱导系统》首个实现停车场无感支付'
      },{
        url: 'http://pbs51uiv3.bkt.clouddn.com/iocn_dwhz@2x.png',
        url1: 'http://pbs51uiv3.bkt.clouddn.com/iocn_handshake@2x.png',
        title:'对外合作',
        desc: '为更多的大数据平台提供更多专业技术服务'
      }
      ]
    }
  },
  components: {
    swiper,
    swiperSlide,
    mainFirst1,
    mainFirst2,
    mainFirst3,
    mainFirst4
  },
  methods: {
      changedd:function(index){
             this.changed=index
             switch (index) {
            case 0:
                this.isshow=true,
                this.isshow1=false,
                this.isshow2=false,
                this.isshow3=false
                break;
            case 1:
                this.isshow=false,
                this.isshow1=true,
                this.isshow2=false,
                this.isshow3=false
                break;
            case 2:
                this.isshow=false,
                this.isshow1=false,
                this.isshow2=true,
                this.isshow3=false
                break;
            case 3:
                this.isshow=false,
                this.isshow1=false,
                this.isshow2=false,
                this.isshow3=true
                break;
            default:
                break;
        }
        },
        //鼠标移除
       mouseLeave:function(){
            this.isActive = null;
      },
    //   点击按钮
    changeCss: function (index) {
        this.changed=index
        switch (index) {
            case 0:
                this.isshow=true,
                this.isshow1=false,
                this.isshow2=false,
                this.isshow3=false
                break;
            case 1:
                this.isshow=false,
                this.isshow1=true,
                this.isshow2=false,
                this.isshow3=false
                break;
            case 2:
                this.isshow=false,
                this.isshow1=false,
                this.isshow2=true,
                this.isshow3=false
                break;
            case 3:
                this.isshow=false,
                this.isshow1=false,
                this.isshow2=false,
                this.isshow3=true
                break;
            default:
                break;
        }
    }
  }
}
</script>
<style>
@media screen and (max-width:1300px){ 
    /* --如果浏览器小于1400px  */
    .main-first .first-top{
        padding: 0 15%;
    }
}
.main-first{
    width: auto;
    background-color: white;
    /* text-align: center; */
}
.first-top{
    min-height: 192px;
    height: auto;
    background-color: #409EFF;
    margin-top: 50px;
    text-align: center;
    padding: 0 26%;
}
.first-top-center{
    min-width: 800px;
    min-height: 192px;
    text-align: center;
    width: auto;
    height: auto;
}
.first-top .first-top-nav1{
    width: 185px;
    min-height: 192px;
    height: auto;
    background-image: url(http://pbs51uiv3.bkt.clouddn.com/bg_lsbj@2x.png);
    background-repeat: no-repeat;
    background-size: 100% 100%;
    text-align: center;
    float: left;
}
.first-top .first-top-nav2{
    width: 185px;
    min-height: 217px;
    height: auto;
    background-image: url(http://pbs51uiv3.bkt.clouddn.com/bj_hskp@2x.png);
    background-repeat: no-repeat;
    background-size: 100% 100%;
    text-align: center;
    float: left;
    margin-top: -25px;
    font-size: 18px;
}
.first-top .first-top-nav2 ul{
    padding: 0 10px;
    color: #fff;
}
.first-top .first-top-nav1 ul{
    padding: 0 10px;
    color: #fff;
}
.first-top-nav1 #nav-title{
    margin-top: 5px;
    margin-bottom: 5px;
}
.first-top-nav1 #nav-descript{
    font-size: 14px;
}
</style>
