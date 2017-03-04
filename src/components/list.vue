<template>
 	<div class="jumbotron">
        <h1>点一下</h1>
        <p v-on:click="show=!show"><router-link to="/list/lists" class="btn btn-lg btn-success" role="button">
				点开
        </router-link></p>
      
    	<span>这里显示</span>
    	<router-view v-if="show"></router-view>
 	</div>
</template>

<script>
export default {
  name: 'jumbotron',
  data () {
    return {
      show: false
    }
  },
 
}
</script>
