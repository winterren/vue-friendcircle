<template>
  <div class="post">
    <!-- 左侧头像 -->
    <div class="left">
    	<div class="avatar">
    		<img :src="data.imgUrl" >
    	</div>
    </div>
    <!-- 右侧 -->
    <div class="right">
    	<div class="post-name">
    		{{ data.name }}
    	</div>
    	<div class="post-text">
    		{{ data.content.text }}
    	</div>
    	<!-- 图片 -->
    	<div class="post-pic">
    		<img  class="full-picture"
    		        v-if="picture.imgUrl"
    		          v-for="picture in data.content.picture"
    		            :src="picture.imgUrl"
    		              :key="picture.id" >
    	</div>
    	<!-- 链接 -->
    	<div class="post-digest"  v-if="data.content.link.time">
    	  <img :src="data.content.link.imgUrl" >
    	  <div> {{ data.content.link.text }} </div>
    	</div>
    	<!-- 发表时间和评论按钮 -->
    	<div class="post-time-ico">
    		<div class="post-time">
    			{{ data.content.location }}
    		</div>
    		<i class="post-icon iconfont icon-comment" v-on:click.stop="onCommentClick"></i>
    		<!-- 评论按钮按后弹 -->
    		<div class="comment-wrapper" :class="{'comment-show': isShow}">
    		  <div class="like" v-on:click="like">
    		    <i class="iconfont icon-like"></i>赞
    		  </div>
    		  <div class="comment">
    		    <i class="iconfont icon-comment"></i>评论
    		  </div>
    		</div>
    	</div>
    	<div class="post-bottom" >
    		<div class="post-like">
    		  	<span   v-bind:class="{'inotlike':notLike}"><i class="iconfont icon-like"></i></span>
    			<span  v-for="like in data.content.like">{{ like.userName }}, </span>
    		</div>
    		<div class="post-comment" v-for="comment in data.content.comment">
    				<span class="username"> {{ comment.username }}
    			  	<span class="reply-entry">
    			    <span class="reply black" v-if="comment.to">回复</span>
    			    <span class="reply-username"> {{ comment.to }} </span>
    			  </span>
    			</span>:
    			<span class="black"> {{ comment.reply }} </span>
    		</div>
    	</div>
    </div>
  </div>
</template>
<script>
    export default {
    	data:function(){
    		return { isShow:false, notLike:true}
    	},
        props:['data'],
        methods:{
        	onCommentClick:function(){
        		this.isShow=(this.isShow?false:true);
        		console.log(this.isShow);
        	},
        	like:function(){
        		this.notLike=(this.notLike?false:true);
        		console.log(this.notLike);
        	}
        }
    }
</script>
<style scoped>
	.post:after{
		clear:both;
		content:'.';
		height: 0;
		display: block;
		visibility: hidden;
	}
	.post{
		margin-top:15px;
	}
/*左侧头像*/
    .left{
    	float: left;
    	padding: 0 10px;
    }
    .avatar img{
		width: 55px;
		height:55px;
    }
/*右侧内容*/
    .right{
    	/*float: left;*/
    	/*width: 100%;*/
    	margin-left:  75px;
    }

    /*姓名*/
    .post-name{
    	color:#1e4c97;
    	font-size:13px;
    }
    .post-text{
    	margin-top:3px;
		font-size:13px;
    }
    /*图片*/
    .post-pic {
    	margin-top: 5px;
    }
    .post-pic img{
    	margin-right: 5px;
    	width: 80px;
    	height: 80px;
    }
    /*链接*/
    .post-digest{
    	background: #f3f3f5;
		height: 55px;
		margin-right: 10px;

    }
    .post-digest img{
    	padding: 5px;
    	float: left;
    	width: 45px;
    	height: 45px;
    }
    .post-digest div{
    	font-size:13px;
    }
    /*时间*/
    .post-time-ico{
    	height: 25px;
    }
    .post-time{
    	float: left;
    	margin-top: 5px;
    	font-size: 12px;
    	color: #757575;
    }
    /*图标*/
    .inotlike{
    	color:rgb(243, 243, 243);
    	text-shadow:#1e4c97 1px 0 0,#1e4c97 0 1px 0,#1e4c97 -1px 0 0,#1e4c97 0 -1px 0;
    }
    .post-icon{
    	color: #92abd4;
    	float: right;
    }
    .post-icon:after{
    	visibility: hidden;
    	content: '.';
    	clear: both;
    	height: 0;
    }
    /*弹出block*/
    .comment-wrapper{
        height: 25px;
    	display: none;
    	position: absolute;
    	width: 120px;
    	background:  rgba(27,27,27,0.8);
    	color: #FFF;
    	right: 30px;
    }
    .like,.comment{
        line-height: 25px;
        text-align: center;
    	width: 50px;
    	display: inline-block;
    	font-size:12px;
    }
    .comment-show{
    	display: block;
    }

    /*评论区*/
    .post-comment{
    	margin-top: 2px;
    }
    .post-bottom{
    	background: #f3f3f3;
    	font-size:12px;
		color:#1e4c97;	
		padding: 5px;
    }
    .black{
    	color:#000;
    }
</style>