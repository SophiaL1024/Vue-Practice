<template >
<form @submit.prevent="add">
  <input v-model='newSong'>
  <button>Add to the list</button>
</form>
</template>
<script>
export default {
  name:'Form',
  data(){
    return {newSong:''};
  },
  methods:{
   add(){
     this.$emit('addNewSong',this.newSong)
     this.newSong='';
   }
  }
}
</script>
<style >
  
</style>