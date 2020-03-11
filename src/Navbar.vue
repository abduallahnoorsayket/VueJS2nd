<template>
  <nav  >
      <h2>Menu for what do you want?  </h2>
   <ul>
    <li> <a href="">Home </a> </li>
    <li> <a href="">About </a> </li>
    <li> <a href="">contact </a> </li>


    </ul>

</nav>    

    
</template>

<script>
export default{

name: 'navbar',
 data(){
     return{

     }
 }

}

</script>



<style scoped >

nav {

    text-align: center;
}
nav ul{
    padding: 0;
}

nav li{

    display: inline-block; 
    list-style-type: none;
    margin: 0;
}

</style>