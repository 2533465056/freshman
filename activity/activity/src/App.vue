<template>
  <div id="app"> 
   <router-view></router-view> 
    <mask-view ref="mask"></mask-view>
    
  </div>
 
</template>


 
<script>
import maskView from "./components/glocal_mack.vue"  

export default {  
  name: 'app',
  components:{
    "mask-view":maskView
  },
  mounted:function(){
    console.log(this.$refs.mask)
  },
  /*watch:{
    "$route":function(){
      this.$refs.mask.show()
     
    }
  },*/
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<style>


*{
  margin:0;
  padding:0;
}
html,body{
  width:100%;
  height:100%;
}
body{
  background:url("imgs/bg.jpg") no-repeat;
  background-size: cover !important;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
   height:100%;
  
}

</style>
