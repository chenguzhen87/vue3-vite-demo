<template>
  <h1>{{ msg }}</h1>
  <button @click="count++">count is: {{ count }}</button>
  <p>Edit <code>components/HelloWorld.vue</code> to test hot module replacement.</p>
  <VideoEditingTimeline :config="config"  />
</template>

<script>
import VideoEditingTimeline from 'video-editing-timeline-vue';
export default {
  name: 'HelloWorld',
  components: {
    VideoEditingTimeline
  },
  props: {
    msg: String
  },
  data() {
    return {
      count: 0,
      age: 10
    }
  },
  setup() {
    return {
       config: {
            canvasWidth: 5000,
            canvasHeight: 50,
            minimumScale: 10, // 一个小刻度长度(单位px)
            minimumScaleTime: 1, // 一个小刻度代表时间（单位秒）
       }
    }
    // setup中不能访问this
    console.log(this)
  },
  mounted(){
    // this 是一个Proxy对象，vue2.x是组组件实例对象
     // console.log(this)
  },
  methods: {
    test(){
      
    },
     onClick(){
      console.log("onclick")
    }
  }
}
</script>
