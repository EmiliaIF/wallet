<template>
  <main class="Addcard">
      <h1>Add a new card</h1>
      <button @click="currentView">Add card</button>
  </main>
</template>

<script>
export default {
  data(){return{

  }},

  methods:{
    currentView(){
      this.$emit('switchviewcard')
    },
  }

}
</script>
<style>

</style>