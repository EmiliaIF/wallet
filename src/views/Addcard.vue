<template>
  <main class="Addcard">
      <h1>Add a new card</h1>
      <Card/>
      <Cardform/>
      
      <button @click="currentView">Add card</button>
  </main>
</template>

<script>
import Cardform from '../components/Cardform.vue'
import Card from '../components/Card.vue'
export default {
  components: { Cardform, Card, },
  data(){return{

  }},

  methods:{
    currentView(){
      this.$emit('switchviewcard')
    },
  }

}
</script>
<style scoped>



</style>