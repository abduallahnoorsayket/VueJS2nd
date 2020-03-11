<template>
    <div class ="blogs">
        <h2> Blogs</h2> 
        <input type="text" v-model="searchTerm">
        <div v-for="post  in filteredPosts" :key="post.id">
        <p> {{post.title}} </p>
        <p> {{post.body | snippet }} </p>
        </div>

        <!-- <h2> {{blogTitle}}</h2> -->
        <!-- <button @click="changeTitle"> change Title </button> -->
        </div>
</template>


<script>
import axios from 'axios'
export default {
    name:'Blogs',
    data(){

        return{
            posts:[],
            searchTerm: ''


            // blogTitle :'Blogs  for sayket'
        }  
    },
    methods:{
        //   changeTitle(){
        //       this.blogTitle='Amazing blogsite !!'
        //   }
    },

    computed:{

        filteredPosts(){
            return this.posts.filter(post =>{
                return post.titlematch(this.searchTerm )

            } )
        }




    },


    // beforeCreate(){

    //     alert('Before create Hooks ')
    // },
    created (){
        axios.get('https://jsonplaceholder.typicode.com/todos/')
       .then(response=>{
           console.log(response)
           this.posts = response.data
       }).catch(err=>{
           console.log (err)
       })
    }
    //   beforeUpdate(){
    //      alert('before Update  hook s')


    // }
      
}  
</script>  