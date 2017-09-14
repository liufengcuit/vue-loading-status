<template>
	<div class="loading">
		<div class="load_animate">
			<span class="data-custom-animate" v-for="loadlist in loadAnimate"></span>
			<p>Loading...</p>
			<p v-text='com'></p>
			
		</div>
	</div>
</template>
<script>
	export default {
		name:'loading',
		data(){
			return {
				loadAnimate:[0,1,2,3,4],
			}
		},
		props:['com'],
		methods:{
			stepLoading:function(){
				var time = setInterval(function(){

				},200);
			}
		},
		mounted(){
			console.log(this.com);
		},
		watch:{
			com:function(n,o){
				console.log(n,'------',o)
			}
		}
	}
</script>
<style scoped>
	.load_animate span{
		display: inline-block;
		width: 12px;
		height: 12px;
		border-radius: 50%;
		background: #ababab;
		margin: 0 5px;
	}
	.load_animate span:first-child{
		width: 16px;
		height: 16px;
	}
	.load_animate .data-custom-animtae-active{
		width: 16px;
		height: 16px;
	}
</style>