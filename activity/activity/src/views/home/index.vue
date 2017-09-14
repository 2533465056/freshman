<template>
	<div class="home">
	  	<div class="person">
	     	 <router-link :to="{name:'question',params:{step:1},query:{type:1}}"><div class="f_like"></div></router-link>
	      	<router-link :to="{name:'question',params:{step:1},query:{type:0}}"><div class="f_wenke"></div></router-link>
	    </div>
   </div>
</template>
<script>
	export default{
		data:function(){
			return{

			}
		}

	}



</script>


<style>
	.home{
		width:100%;
		height:100%;
	}
	.person{
	  width:84%;
	  height:100%;
	  background:url("../../imgs/home-pepole.png") no-repeat center top;
	  background-size: 100% 432px;
	  margin:0 auto;
	  position: relative;
	}
	.f_like,.f_wenke{
	  position: absolute;
	  width:30%;
	  height:50px;
	  top:250px;
	}
	.f_like{
	   background:url("../../imgs/f-like.png") no-repeat center center;
	    background-size:contain;
	    left:10%;
	}
	.f_wenke{
	   background:url("../../imgs/f-wenke.png") no-repeat center center;
	    background-size:contain;
	    right:10%;
	}


</style>