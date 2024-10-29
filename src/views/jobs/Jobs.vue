<template>
    
    <h1>THE JOBS</h1>
    <div v-for="job in jobs" :key="job.id">
        <router-link :to="{name : 'JobDetails',params : {id : job.id}}">
            <h3>{{ job.title }}</h3>
        </router-link>
       
      </div>
    
 
</template>

<script>
export default {
data(){
    return{
        jobs :[]
    }
},
mounted(){
    fetch('http://localhost:3000/jobs')
    .then(res => res.json())
    .then(data => this.jobs = data)
    .catch(err => console.log(err.message))
}
}
</script>

<style scoped>
 h1{
  text-align: center;
  color:white;
  background-color: rgb(206, 27, 27);
  padding :20px;
  width:20%;
  margin: 0 auto;
 }
 div{
  text-align: center;
  background-color: rgb(191, 187, 187);
  padding: 20px;

  margin:30px auto;
  width: 30%;
 } 

 div a{
    text-decoration: none;
    color: black;
 }
</style>