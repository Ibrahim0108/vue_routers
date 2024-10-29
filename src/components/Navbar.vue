<template>
  <nav>
    <ul>
         <li> <RouterLink to="/">Home</RouterLink></li>|
         <li> <RouterLink to="/about">About</RouterLink> </li>|
         <li> <RouterLink to="/jobs">jobs</RouterLink> </li>
        </ul>
   
      </nav>
</template>

<script>
export default {

}
</script>

<style scoped >
nav{
  font-size: larger;
  margin-bottom: 40px;
  
}

li{
  display: inline;
  margin-right: 10px;
  text-align: center;
  
}
li a{
  text-decoration: none;
  color: black; 
}
ul{
  
  list-style : none;
}
.router-link-active{
  color :white;
  font-weight: bold;
  background-color: red;
  padding: 10px;
  border-radius: 4px;
}

</style>