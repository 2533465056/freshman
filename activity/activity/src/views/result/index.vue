<template>
	<div class="box">
		<img src="../../imgs/seal.png" alt="" class="pic1">
		<h4>{{res.name}}</h4>
		<span>{{res.subject}}{{res.majors}}{{res.character}}{{res.shareTxt}}</span>
		<img src="../../imgs/btn-intr.png" alt="" class="pic2">
		<img src="../../imgs/btn-share.png" alt="" class="pic3">
			
	</div>
</template>


<script>
	export default{
		data:function(){
			return {
				res:""
			}
		},
		created:function(){
			this.$http.get("../../src/service/school_list.json").then((res)=>{

					this.res=res.data[this.random()]
					
				})
		},
		methods:{
			random(min=1,max=11){
				let num=Math.floor(Math.random()*max-min)
				if(num<10){
					num="0"+num
				}
				return 'school'+num
			}
		}

		
	}
</script>
 
<style>
.box{
	background: url('../../imgs/bg-matriculate.png')no-repeat ;	background-size: 100% 100%;
	height: 56%;
	width: 80%;
	margin: 30px auto;
}
.pic1{
	position: absolute;
    right: 3%;
    top: 4px;
    width: 29%;
}
h4{
	position: absolute;
    left: 43%;
    top: 115px;
}
span{

	
       text-align: center;
    position: absolute;
    top: 198px;
    width: 70%;
    margin-left: 3px;
    left: 59px;

}
.pic2{
	width: 28%;
    position: absolute;
    top: 315px;
    left: 15%
}
.pic3{
	width: 28%;
    position: absolute;
    top: 315px;
    right: 15%
}

</style>
