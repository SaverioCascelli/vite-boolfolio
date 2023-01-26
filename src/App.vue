<script>

import axios from 'axios';

export default{
  name:'App',
  data(){
    return{
      url: 'http://127.0.0.1:8000/api/projects',
      projects:[],
   }
  },
  methods:{
    getApi(){
      axios.get(this.url)
        .then(result =>{
          this.projects = result.data;
          console.log(result.data);
        })
    }
  },
  mounted(){
    this.getApi();
  }

}


</script>

<template>
  

</template>

<style scoped lang="scss">
@use './style/general.scss';
</style>
