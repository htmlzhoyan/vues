<template>
  <div id="wrapper">
    <nav class="navbar navbar-default">
        <div class="container-fluid">
          <div class="navbar-header">
            <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#navbar" aria-expanded="false" aria-controls="navbar">
              <span class="sr-only"></span>
              <span class="icon-bar"></span>
              <span class="icon-bar"></span>
              <span class="icon-bar"></span>
            </button>
            <a class="navbar-brand" href="#">{{$store.state.totalTime}}</a>
          </div>
          <div id="navbar" class="navbar-collapse collapse">
            <ul class="nav navbar-nav">
              <li><router-link to="/home">首页</router-link></li>
          	<li><router-link to="/time-entries">计划列表</router-link></li>
            	<li><router-link to="/list">list</router-link></li>
              <li class="dropdown">
                <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Dropdown <span class="caret"></span></a>
               
              </li>
            </ul>
            <ul class="nav navbar-nav navbar-right">
              <li class="active"><a href="./">Default <span class="sr-only">(current)</span></a></li>
              <li><a href="../navbar-static-top/">Static top</a></li>
              <li><a href="../navbar-fixed-top/">Fixed top</a></li>
            </ul>
          </div><!--/.nav-collapse -->
        </div><!--/.container-fluid -->
      </nav>
    <div class="container">
    	
      <div class="col-sm-3">
        <sidebar v-bind:xu="total"></sidebar>
        <foo txt="我是底部" v-bind:dddd="bentext" boos="555" v-on:ee="incrementTotal"></foo>
        <input type="text" v-model="bentext"/>
       	<p>{{total}}</p>
      </div>
      <div class="col-sm-9">
        <router-view></router-view>
      </div>
    </div>
  </div>
</template>

<script>
import Sidebar from './components/Sidebar.vue'
import foo from './components/foo.vue'
export default {
  name: 'app',
  components: {
    Sidebar,foo
  },
  data(){
  	return{
  		bentext:"Hello evety",
  		total:"20"
  	}
  },
  methods:{
  	incrementTotal:function(b){
  		this.total=b
  	}
  }
}
</script>

<style>
	
	
</style>