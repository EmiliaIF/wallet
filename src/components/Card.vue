<template>
  <div class="Creditcard">


    <div class="top">
      <img src="../assets/wifi.svg" alt="">
      <img class="bitcoin" src="../assets/bitcoin.svg" alt="bitcoin">
    </div>

    <div class="chip">
    <img src="../assets/chip.svg" alt="">
    </div>

    <div class="cardnumber">
      <p>{{importData.cardNumber | spacedout}}</p>
    </div>

      

    <div class="spaced">
      <div class="text">
      <p>CARDHOLDER NAME</p>
      <p>{{importData.cardholder}}</p>
      
      
    </div>

    <div class="text2">
      <p>Month /  Year</p>
      <p>{{importData.expireMonth}} / {{importData.expireYear}}</p>
      
    </div>
   
  </div>
  </div>
</template>

<script>

export default {
  

  filters:{
  spacedout(value){
    if (!value) {
        return "XXXX XXXX XXXX XXXX";
      }
const parts = value.match(/.{1,4}/g);
      return parts.join(" ");
}},
  
  components: {},
  props:[ "importData"],
  data(){return{


  }
  
  }

}
</script>

<style>

.Creditcard{

    width: 382px;
    height: 241px;
    background-color: cadetblue;
    border-radius: 5px;
    margin-left: 20px;
    display: flex;
    flex-direction: column;
    

}
.cardnumber{
   display: flex;
    flex-direction: row;
    justify-content: center;
    margin-left: 1rem; 
}
.chip{
  display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-left: 1rem; 
}
.spaced{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  
}


.top{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    margin-left: 1rem;
    margin-right: 1rem;
    margin-top: 1rem;
    margin-bottom: 0px;
    
}

.bitcoin{
  width: 50px;
  height: 50px;
 
}
.text2{
  
    /* display: flex;
    flex-direction: column;
    justify-content: flex-end; */
    margin-left: 1rem;
    margin-right: 1rem;
}

.text{

    
    margin-left: 1rem;
    margin-right: 1rem;
    
}

</style>