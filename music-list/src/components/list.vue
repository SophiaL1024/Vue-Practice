<template >
  <div>
    <ul id='list' v-if='musicList.length'>
      <li v-for='(item, index) of musicList' :key='index'>No. {{index+1}} {{item}}</li>
    </ul>
    <h3 v-else>There is no music input yet.</h3>
  </div>
</template>
<script>
export default {
  name:"List",
  props:['musicList']  
}
</script>
<style >
  #list{
 list-style-type: none;  
  }
</style>