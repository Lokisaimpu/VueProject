<template>

    <div v-for="Restaurant of Restaurants" :key="Restaurant.id">
        <SingleBook :Restaurant=Restaurant />

    </div>
</template>

<script>
import SingleBook from './SingleBook.vue'
      export default{
        name: 'BookBox',
        props:{
            Restaurants: Array
        },
        components:{
            SingleBook
        }
      }
</script>

<style scoped>
.bookbox{

    background-color: rgb(86, 74, 143);
    padding: 1em;
    color: rgb(240, 41, 41);
    margin: auto;
}
</style>
