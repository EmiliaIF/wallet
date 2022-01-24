<template>
  <div id="app">
    <nav>
      
      
    </nav>
    
    <Home v-if="currentView == 'Home'" @switchviewhome="currentView = 'Addcard'"/>
    <Addcard v-else-if="currentView == 'Addcard'" @switchviewcard="currentView = 'Home'"/>
    <!-- <Cardform/> -->
    
  
  </div>
</template>

<script>
import Home from './views/Home.vue'
import Addcard from './views/Addcard.vue'



export default {
  components: { Home, Addcard,},
  name: 'App',
  data(){ return {
    currentView : 'Home'
  }}
}
</script>





<style>
@import url('https://fonts.googleapis.com/css2?family=Ropa+Sans&family=Source+Sans+Pro&display=swap');

@import url('https://fonts.googleapis.com/css2?family=Ropa+Sans&family=Source+Sans+Pro&display=swap');

body{
  display: flex;
  align-items: center;
  flex-direction: column;
  background-color: bisque;

}



#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 10px;
  margin-bottom: 10px;
  display: flex;
  flex-direction: column;
  align-items: center;
  
  
  
  width: 414px;
  height: 896px;
  background-color: white;

}
/* a{
  margin: 2rem; */
/* } */
h1{
font-family: 'Source Sans Pro', sans-serif;
font-weight: 900;

}
button{
background-color: white;
  border: 2px solid #555555;
  padding: 15px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin-top: 10px;
  cursor: pointer;
  
}

p,button,input{

font-family: 'Source Sans Pro', sans-serif;
}

</style>
