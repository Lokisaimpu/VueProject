<template>
    <div>
    <h2>{{ Restaurant.title }}</h2>
    <h4>{{ Restaurant.location }}</h4>
    <h4>Michelin Stars: {{ Restaurant.Michelin_stars }}</h4>
    <h4>Year Founded: {{ Restaurant.Year_Founded }}</h4>
    <h4>Annual Revenue: {{ Restaurant.Annual_Revenue }}</h4>
    <h4>Specialties: {{ Restaurant.Specialties }}</h4>
    <h4>Daily Customer Count: {{ Restaurant.Average_Daily_Customer_Count }}</h4>
    <h4>Ratings: {{ Restaurant.Ratings }}</h4>
  </div>
</template>

<script>
export default{
    name: 'SingleBook',
    props:{
        Restaurant: Array
    }
  
}

</script>

<style scoped>

h4 {
    margin: 4px;
}

h2 {
    margin-bottom: 10px; /* Add margin to separate the title from other details */
} 

div {
    background-color: #c2f0f0;
    padding: 1em;
    text-align: center;
    width: 80%;
    margin: auto;
}

.red {
    background-color: rgba(180, 210, 247, 0.412) !important;
}

</style>
