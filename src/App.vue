<template>
  <div id="app">
    <div v-for="(item,index) in data" :key='index'>
      <HelloWorld msg="Welcome to Your Vue.js App"/>
    <button @click="handleDel(index)">del</button>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data(){
    return {
      data:[
        { name: "ftd1" },
        { name: "ftd2" },
        { name: "ftd3" },
        { name: "ftd4" },
        { name: "ftd5" },
        { name: "ftd6" },
        { name: "ftd7" },
        { name: "ftd8" }
      ]
    }
  },
  methods:{
    handleDel(index){
      this.data.splice(index,1)
    }
  }
}
</script>

<style>
</style>
