<template>
  <div id="header">
    <div id="container">
    	<i class="iconfont icon-back"></i>
    	<span class="title">朋友圈</span>
    	<input type="file" class="iconfont icon-camera right"></i>
    </div>
  </div>
</template>
<script>
    export default {
        
    }
</script>
<style scoped>
	#header{
		height: 45px;
	}
    #container{
    	height: 45px;
    	width: 100%;
    	background: #1b1b1b;
    	position: fixed;
    	line-height: 45px;
    }
    .iconfont,.title{
    	color: white;
    	margin:0 5px;
    }
    .right{
        margin-top:10px;
        width: 22px;
        height: 17px;
        display: inline-block;
    	float: right;
    	margin-right: 11px;
    }
</style>