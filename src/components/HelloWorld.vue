<template>
  <h1>{{ msg }}</h1>
  <button @click="count++">count is: {{ count }}</button>
  <p>Edit <code>components/HelloWorld.vue</code> to test hot module replacement.</p>
  <Test @onChange="onChange" id="ddd" :age="age"/>
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
  methods: {
    onChange(){}
  }
}
</script>
