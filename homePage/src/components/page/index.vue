<template>
<div>
    <indexNav></indexNav>
</div>
</template>
<script>
import indexNav from '@/components/common/indexNav'
export default {
	data(){
		return{
			screenWidth: document.body.clientWidth   // 这里是给到了一个默认值 （这个很重要）
		}
	},
	components:{
		indexNav
	}
}
</script>
<style>
/* @media screen and (min-width: 320px) and (max-width: 1156px){
			  .site-bg-dl {
			  position: fixed;
			  height: 100%;
			  width: 100%;
			  z-index: 0;
			  background-size: cover;
			  background-repeat: no-repeat;
			  background-attachment: fixed;
			  background-size:100% 100%;
			  -moz-background-size:100% 100%;
			}
} */
</style>
