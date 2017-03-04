<template>
  <div class="panel panel-default">
    <div class="panel-heading">
      <h1 class="text-center">已有时长{{$store.state.totalTime}}</h1>
      <h1 class="text-center">已有时长{{xu}}小时</h1>
      <p>{{xu}}</p>
    </div>

    <div class="panel-body">
   <iframe frameborder="no" border="0" marginwidth="0" marginheight="0" width=300 height=86 src="//music.163.com/outchain/player?type=2&id=439915614&auto=1&height=66"></iframe>
    </div>

  </div>
</template>
<script>
    export default {
      name : 'Sidebar',
      props:['xu'],
      data(){
      	return{
					score:20,			
				}
      },
     methods:{
		  	
		  	increment:function(b){
  				
		  				this.score=b
		  		
  			}
		  }
     
    }
</script>
