<script>

import Navbar from './components/Navbar.vue';

export default{
  components:{Navbar},
  methods : {
        redirect(){
          this.$router.push({name : 'home'})
        },
        back(){
          this.$router.go(-1)
        },
        forward(){
          this.$router.go(1)

        }
}
}

</script>


<template>
 
 <div>

 <Navbar/>

<section>
  <button @click="redirect">redirect</button>
  <button @click="back">go back</button>
  <button @click="forward">go forward</button>

  <RouterView />
</section>
</div>
</template>


<style scoped>
button{
margin-right: 10px;
padding : 10px;
background-color: rgb(218, 215, 215);
color: red;
font-weight: bold;
border: none;
}
</style>
