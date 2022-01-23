<template>
  <div>
    <!-- <Card/> -->
  <form @submit.prevent="" class="Cardform">
    
    <input type="text"  placeholder="Card number">
    <input type="text"  placeholder="Cardholder name">

    <div class="monthyear">
    <input type="text" placeholder="Month">
    <input type="text" placeholder="Year">
    </div>

    <div class="dropdown">
      <button class="dropbtn">Month</button>
        <div class="dropdown-content">
          <a href="#">Link 1</a>
          <a href="#">Link 2</a>
          <a href="#">Link 3</a>
        </div>
      </div>
   
  </form>
 </div>
</template>

// <script>
// import Card from '../components/Card.vue'
// export default {
//   components: { Card,},
//    data(){return{

//   }},


// }
</script>

<style >
form{
    
    display: flex;
    flex-direction: column;
    align-items: center;
    box-sizing: border-box;
    
}
.monthyear{
  width: 100%;
  display: flex;
  flex-direction: row;
  margin-left: 35%;
}

.monthyear input{
  width: 100px;
  
  
}




input{

  width: 382px;
  border-radius: 5px;
}

input[type=text] {
  background-color: white;
  background-repeat: no-repeat;
  margin: 1rem;
  height: 40px;
  
}

input.dropbtn {
  background-color: white;
  color: black;
  border: 2px solid black;
  font-size: 16px;
  
  height: 40px;
  align-items: center;
  margin: 0;
}


.dropdown {

  display: inline-block;
  width: 180px;
  
}


.dropdown-content {
 
  display: none;
  position: absolute;
  background-color: #f1f1f1;
  width: 175px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
}


.dropdown-content a {
  color: black;
  padding: 12px 16px;
  text-decoration: none;
  display: block;
}

.dropdown-content a:hover {background-color: #ddd;}


.dropdown:hover .dropdown-content {display: block;}


.dropdown:hover .dropbtn {background-color: rgb(201, 201, 201);}

</style>