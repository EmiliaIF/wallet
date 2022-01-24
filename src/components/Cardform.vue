<template>
  <div>
    <Card :importData ="cardInfo"/>

  <form @submit.prevent="" class="Cardform">
    
    <input @keypress="cardlength"   v-model="cardInfo.cardNumber" type="number"  placeholder="Card number">
    <input v-model="cardInfo.cardholder" type="text"  placeholder="Cardholder">

    <div class="monthyear">
    <div class= "month">
    <p>Month</p>
    <input @keypress="monthlength"  v-model="cardInfo.expireMonth" type="number" placeholder="Month">
    </div>
    <input @keypress="monthlength" v-model="cardInfo.expireYear" type="number" placeholder="Year">
    </div>

    <div class="dropdown">
      
        <select name="dropdown-content" id="dropdown-content">
          <option value="Bitcoin">Bitcoin Inc</option>
          <option value="Evil">Evil Corp</option>
          <option value="Ninja">Ninja Bank</option>
          <option value="Block">Block Chain Inc</option>
        </select>
      </div>
   
  </form>
 </div>
</template>

// <script>
import Card from './Card.vue'
export default {
  components: { Card, },
  data(){return{
  cardInfo:{
  cardNumber: "", 
  cardholder: "", 
  expireMonth: "", 
  expireYear: "", 
  vendor: "", 

   }}},

methods:{
  cardlength(number){
    const maxNum = number.target.value;
    if(maxNum.length >= 16) {
    number.preventDefault();
    }
  },
  monthlength(number){
    const maxNum = number.target.value;
    if(maxNum.length >= 2){
      number.preventDefault();
    }
  },
  
}

}
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
/* .month{
 display: flex;
flex-direction: column;
margin: */

/* } */



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

input[type=number] {
  background-color: white;
  background-repeat: no-repeat;
  margin: 1rem;
  height: 40px;
  
}


select{
  background-color: white;
  color: black;
  border: 2px solid black;
  font-size: 16px;
  
  height: 40px;
  align-items: center;
  margin: 0;
  width: 242px;
  border-radius: 5px;
}


option {
 
  background-color: rgb(73, 73, 73);
  width: 175px;
  box-shadow: 0px 8px 16px 0px rgba(0,0,0,0.2);
  z-index: 1;
  border-radius: 5px;
  color:white;
}



</style>