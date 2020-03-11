<template>
  <div id="app">
    <br>
    <br>
    <br>
    <br>
    
    <h1>{{title | upp}}</h1>

    <Navbar />

    <Blogs/>

  </div>
  
</template>

<script>
import Navbar from '../src/Navbar'
import Blogs from '../src/assets/Blogs'

export default{

name: 'app',
 components:{Navbar,Blogs} ,  
 data(){
     return{
       title:"Please help me "
     }
 },
//  filters:{
//    upp:function(v){
//      return v.toUpperCase()
//    }
//  }

}
</script>

  
<style>
h1{
  color: #444;
  font-weight: normal;
  text-align: center;
  }
</style>
