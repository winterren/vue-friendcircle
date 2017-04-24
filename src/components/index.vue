<template>
  <div id="circle">
  	<headersection></headersection>
  	<wallpaper v-bind:data="data"></wallpaper>
  	<contentsection v-bind:data="data"></contentsection>
  </div>
</template>
<style scoped>
    
</style>
<script>
	import headersection from './main/header.vue'
	import contentsection from './main/content.vue'
	import wallpaper from './main/wallpaper.vue'
	import '../assets/css/iconfont.css'
    export default {
    	data: function(){
    		return {data:data};
    	},
        components:{
        	headersection:headersection,
        	wallpaper:wallpaper,
        	contentsection:contentsection
        }
    }

    var data = {
            id: 1917831232,
            name: '武松',
            imgUrl: '/static/wusong.png',
            bg:'/static/tiger.jpg',
            brief: '愿得一人心白首不分离',
            contentList: [
              {
                id: 1997234346,
                name: '李白',
                imgUrl: '/static/libai.png',
                brief: '辰风破浪',
                content: {
                  text: '阁下何不乘风起，扶摇直上九万里。你咋不上天，和神舟十六号肩并肩。',
                  fullText: '全文',
                  picture: [
                    {
                      imgUrl: ''
                    }
                  ],
                  video: '',
                  link: {
                    time: '',
                    imgUrl: '',
                    text: ''
                  },
                  location: '大唐酒吧',
                  time: '刚刚',
                  source: '',
                  like: [
                    {
                      id: '',
                      userName: '杜甫'
                    },
                    {
                      id: '',
                      userName: '陶渊明'
                    },
                    {
                      id: '',
                      userName: '周杰伦'
                    },
                    {
                      id: '',
                      userName: 'JJ'
                    },
                    {
                      id: '',
                      userName: '白百合'
                    },
                    {
                      id: '',
                      userName: '陈羽凡'
                    }
                  ],
                  comment: [
                    {
                      username: '武松',
                      to: '',
                      text: '',
                      reply: '呵呵'
                    },
                    {
                      username: '项羽',
                      to: '',
                      text: '',
                      reply: '上线打王者荣耀'
                    },
                    {
                      username: '杜甫',
                      to: '',
                      text: '',
                      reply: '想你，速回'
                    },
                    {
                      username: '李白',
                      to: '杜甫',
                      text: '',
                      reply: '我也想你'
                    }
                  ]
                }
              },
              {
                id: 19978322567,
                name: '尹志平',
                imgUrl: '/static/yinzhiping.png',
                brief: '我爱台妹',
                content: {
                  text: '我爱台妹 台妹爱我',
                  fullText: '全文',
                  picture: [
                    {
                      id: 1,
                      imgUrl: '/static/yinzhiping1.png'
                    },
                    {
                      id: 2,
                      imgUrl: '/static/yinzhiping2.png'
                    }
                  ],
                  video: '',
                  link: {
                    time: '',
                    imgUrl: '',
                    text: ''
                  },
                  location: '桃花岛',
                  time: '8分钟前',
                  source: 'QQ浏览器',
                  like: [
                    {
                      id: '',
                      userName: '黄蓉'
                    },
                    {
                      id: '',
                      userName: '小龙女'
                    },
                    {
                      id: '',
                      userName: '郭靖'
                    },
                    {
                      id: '',
                      userName: '周伯通'
                    },
                    {
                      id: '',
                      userName: '杜甫'
                    },
                    {
                      id: '',
                      userName: '陈羽凡'
                    }
                  ],
                  comment: [
                    {
                      username: '杨过',
                      to: '',
                      text: '',
                      reply: '混蛋'
                    },
                    {
                      username: '小龙女',
                      to: '杨过',
                      text: '',
                      reply: '过儿乖'
                    },
                    {
                      username: '杜甫',
                      to: '',
                      text: '',
                      reply: '白天不懂夜的黑'
                    },
                    {
                      username: '李白',
                      to: '',
                      text: '',
                      reply: '呵呵~'
                    }
                  ]
                }
              },
              {
                id: 19978329555,
                name: '张无忌',
                imgUrl: '/static/songqingshu.png',
                brief: '搞事情',
                content: {
                  text: '都来参加啊',
                  fullText: '全文',
                  picture: [
                    {
                      imgUrl: ''
                    }
                  ],
                  video: '',
                  link: {
                    time: '2017-04-17',
                    imgUrl: '/static/ad.png',
                    text: '【推广】第二次光明顶大会隆重召开'
                  },
                  location: '光明顶',
                  time: '25分钟前',
                  source: '',
                  like: [
                    {
                      id: '',
                      userName: '杨逍'
                    },
                    {
                      id: '',
                      userName: '蛛儿'
                    },
                    {
                      id: '',
                      userName: '林俊杰'
                    },
                    {
                      id: '',
                      userName: '鹿晗'
                    },
                    {
                      id: '',
                      userName: 'Kobe'
                    },
                    {
                      id: '',
                      userName: 'Durant'
                    }
                  ],
                  comment: [
                    {
                      username: 'Kobe',
                      to: '',
                      text: '',
                      reply: 'I like basketball'
                    },
                    {
                      username: 'Durant',
                      to: 'Kobe',
                      text: '',
                      reply: 'You silly'
                    },
                    {
                      username: 'Kobe',
                      to: 'Durant',
                      text: '',
                      reply: '能说中文不？'
                    },
                    {
                      username: '宋青书',
                      to: '',
                      text: '',
                      reply: '哎~'
                    }
                  ]
                }
              }
            ]
          }
</script>

