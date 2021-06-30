<template>
  <h1>{{ msg }}</h1>
  <button @click="count++">count is: {{ count }}</button>
  <p>Edit <code>components/HelloWorld.vue</code> to test hot module replacement.</p>
  <Test class="test" style="background:red" @test="test" @click="onClick" id="ddd" :age="age"/>
</template>

<script>
import Test from "./Test.vue"
export default {
  name: 'HelloWorld',
  components: {
    Test
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
