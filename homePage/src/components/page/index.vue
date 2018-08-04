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
</style>
