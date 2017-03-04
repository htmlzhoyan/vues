<template>
	<div id="foo">
		<button>{{txt}}</button>
		<p>{{dddd}}</p>
		<p>{{boos}}</p>
		<button v-on:click="increment">{{ counter }}</button>
		
	</div>
</template>
<script>
	export default{
		name:'foo',
		props:['txt','dddd','boos'],
		
		data:function(){
			return{
				counter:20,
				
			}
		},
		methods:{
			increment:function(){
				this.counter+=1
				this.$emit('ee',this.counter)
			},
		
			
			
		},
	}
</script>
<style>
	#foo button{
		background-color:#f60 ;
	}
</style>