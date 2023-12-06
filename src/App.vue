<template>
    <!-- step 3: use the component -->
    <MyHeader projectName="Top 5 Restaurants" authorName="Lokesh Saimpu"/>
    <BookBox :Restaurants="Restaurants" />
</template>

<script>
// Step1: you import the component
import MyHeader from './components/MyHeader.vue'
import BookBox from './components/BookBox.vue'

    export default{
      name: 'App',
      //Step2 : register the component
      components:{
        MyHeader,
        BookBox
      },
      data(){
        return{
          Restaurants: []
        }
      },
      mounted(){
          fetch('https://myproject-unx8.onrender.com/api')
         .then(res=>res.json())
         .then(data=>{this.Restaurants = data.Restaurants;})
         .catch(err=>console.log(err.message))
        }

      


    }

</script>

<style>
  
  @import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  
  body {
    font-family: 'Montserrat', sans-serif;
  }
  .container {
    max-width: 400px;
    margin: 30px auto;
    overflow: auto;
    min-height: 300px;
    border: 0.3em solid black;
    padding: 30px;
    border-radius: 5px;
  }
  
  div{
    margin-bottom: 0.5em;
  
  }
  
  
  </style>
