<template>
<div class="main-first">
            <!-- 图片部分 -->
            <div class="first3-bottom">
                <el-row>
                        <el-col :span="8">
                            <div>
                               <img src="http://pbs51uiv3.bkt.clouddn.com/pic_td01@2x.png">
                            </div>
                        </el-col>
                        <el-col :span="8">
                            <div>
                               <img src="http://pbs51uiv3.bkt.clouddn.com/pic_td02@2x.png">
                            </div>
                        </el-col>
                        <el-col :span="8">
                            <div>
                               <img src="http://pbs51uiv3.bkt.clouddn.com/pic_td03@2x.png">
                            </div>
                        </el-col>
                </el-row>
                <!-- 介绍 -->
                <div class="description">
                    卡莱科技聚集了一批朝气蓬勃、积极向上、勇于创新、敢于挑战的高素质专业型人才，他们有来自互联网领域的高精尖科技型人才，也有来自市场营销的销售精英，在时代与梦想的召唤下，凝聚到一起。
                    我们青春洋溢、我们不畏艰辛，在卡莱科技这艘大船上，乘着大数据时代的东风，我们像勇敢的水手，坚韧果敢地驶向互联网的蓝海。
                </div>
            </div>
        </div>    
</template>
<script>
export default {
    
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
.first3-bottom{
    width: 90%;
    height: 350px;
    text-align: center;
    margin-top: 148px;
    margin-bottom: 140px;
    padding: 0 5%;
}
.first3-bottom img{
    width: 87%;
}
.description{
    text-align: center;
    width: 86%;
    margin-top: 50px;
    padding: 0 7%;
    font-size: 18px;
    font-weight: bold;
}
</style>
