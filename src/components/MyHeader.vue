<template>
       <div>
          <h2>{{projectName}}</h2>
          <h2>{{authorName}}</h2>
          
       </div>
</template>

<script>

    export default{
        name: 'MyHeader',
        props:{
            authorName: String,
            projectName: String
        }
    }
 </script>

<style scoped>
div {
  text-align: center;
  background-color: #adad85;
  padding: 10px; /* Add padding for better visual appearance */
  margin: 5px; 
  width: 80%;
  margin: auto;
}

</style>
