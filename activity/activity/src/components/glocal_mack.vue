<template>
	<div class="mask" :class="{'active':isActive}"> 
		<h1>loading...</h1>
	</div>
</template>


<script>

export default{    
		name:"mask-view",
		data:function(){
			return {
				isActive:false
			}	
		},
		methods:{
			show(){
				this.isActive=true
			},
			hide(){
				this.isActive=false
			}

		}
		
	}

</script>


<style>
	.mask{
		width:100%;
		height:100%;
		position: absolute;
		top:0;
		left:0;
		background: rgba(0,0,0,0.7);
		color:#fff;
		display: none;
	}
	.active{
		display: block;
	}
</style>