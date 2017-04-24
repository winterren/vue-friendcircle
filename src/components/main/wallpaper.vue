<template>
  <div id="header">
    <div id="bg"  :style="{backgroundImage: 'url('+data.bg+')', backgroundSize: width+'px'}" >
    	<div id="ava-con">
    		<img id="ava-pic" v-bind:src="data.imgUrl">
    		<span id="ava-text">{{data.name}}</span>
    	</div>
    </div>
  </div>
</template>
<script>
    export default {
        props:["data"],
        computed:{
        	width:function(){
        		return window.innerWidth;
        	}
        }
    }


</script>
<style scoped>
    #header{
    	height: 290px;
    }
    #bg{
    	display: block;
    	/*background-repeat: no-repeat;*/
    	height: 260px;
    }
    #ava-text{
    	color: #fff;
    	margin-top: 220px;
    	margin-right: 20px;
    	float: right;
    }
    #ava-pic{
    	height: 66px;
    	width: 66px;
    	margin-top: 220px;
    	margin-right: 20px;
    	float: right;
    	border:2px solid #fff;
    	box-shadow: 0px 0px 1px 1px #aaa;
    }
</style>