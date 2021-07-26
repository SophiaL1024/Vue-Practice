<template>
  <div id="app">
  <Form @addNewSong='add'/>
   <List :musicList='musicList'/>
  </div>
</template>

<script >
import List from "./components/list.vue";
import Form from './components/form.vue'

export default {
  name: 'App',
  components: {
  List,
  Form
  },
  data(){
    return {
      musicList:[]
    }
  },
methods:{
  add(arg){
    this.musicList.push(arg);
  }
}
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
