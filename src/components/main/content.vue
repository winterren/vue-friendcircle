<template>
  <div id="content">

  	<contentsection v-for="item in data.contentList" v-bind:data="item"></contentsection>
    
  </div>
</template>
<script>
	import contentsection from './contentsection.vue'
    export default {
        props:['data'],
        components:{
        	contentsection:contentsection
        }
    }
</script>
<style scoped>
    
</style>