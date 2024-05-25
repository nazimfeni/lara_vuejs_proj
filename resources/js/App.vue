<template>
      <div>
        <h1>Hello Vue 3 with Laravel and Vite from App.vue!</h1>
      
      </div>
    </template>
    
<script>
import axios from 'axios';
export default {
  mounted(){
    this.fetcData();
  },
  methods:{
    fetcData(){
      axios.get('api/test-data')
      .then((response)=>{
       alert(response.data.message);
      })
      .catch((error)=>{
            
        console.log(error.data)
      })
    }
  }
}
</script>