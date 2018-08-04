<template>
    <div class="main-first">
            <!-- 图片部分 -->
            <div class="first4-bottom">
                <el-row>
                        <el-col :span="6" v-for="(item,index) in items" :key="index">
                            <div class="mouse1"  :class="{'mouse':index ==isActive}"
                                 :style="{backgroundImage: 'url(' + (index ==isActive ? item.coverImgUrl : item.baseImg) + ')', backgroundSize:'contain'}" 
                                 v-on:mouseenter="changedd(index)" v-on:mouseleave="mouseLeave()"> 
                                <p>
                                    <i :class="item.img"></i><br/>
                                    <span>{{item.title}}</span>
                                </p>
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
            items:[{
                title:'移动应用',
                content:'财务策划',
                img:'icon iconfont icon-pingtaigonghui',
                coverImgUrl:'http://pbs51uiv3.bkt.clouddn.com/ydyy.jpg'
            },
            {
                title:'平面设计',
                content:'财务策划',
                 img:'icon iconfont icon-qianqicehua',
                 coverImgUrl:'http://pbs51uiv3.bkt.clouddn.com/pmsj.jpg'
            },
            {
                title:'网站建设',
                content:'财务策划',
                 img:'icon iconfont icon-bi',
                 coverImgUrl:'http://pbs51uiv3.bkt.clouddn.com/wzjs.jpg'
            },
            {
                title:'微信小程序',
                content:'财务策划',
                 img:'icon iconfont icon-computer',
                 coverImgUrl:'http://pbs51uiv3.bkt.clouddn.com/weChat.jpg'
            }]
        }
    },
    methods:{
        changedd:function(index){
             this.isActive = index;

        },
        //鼠标移除
       mouseLeave:function(){
            this.isActive = null;
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
    width: 100%;
    background-color: #fff;
    text-align: center;
}
.first4-bottom .mouse{
    width: 21.6vw;
    height: 250px;
    /* http://pbs51uiv3.bkt.clouddn.com/pic_XWZX@2x.png */
    background-image:url(http://pbs51uiv3.bkt.clouddn.com/1533115949%281%29.jpg);
    background-repeat: no-repeat;
    background-size: 100% 100%;
    color: rgba(0, 0, 0, 0);
    margin-top: -18px;
}
.first4-bottom{
    width: 90%;
    height: 17vw;
    text-align: center;
    margin: 9vw 0 7vw 0;
    padding: 0 5%;
}
.first4-bottom .mouse1{
    width: 98%;
    height: 15vw;
    text-align: center;
    margin-top: -18px;
}
.first4-bottom p{
    height: auto;
    padding: 5.8vw 0;
    font-size: 1.2vw;
    font-weight: bold;
    line-height: 40px;
}
.first4-bottom p i{
    width: 100%;
    height: auto;
    font-size: 36px;
}
.first4-bottom span{
    padding-top: 10px;
}
</style>
