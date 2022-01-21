<template>
    <main class="Home">
      <h1>E-Wallet</h1>
      <button @click="currentView">Home</button>
  </main>
</template>

<script>
export default {
  data(){return{

  }},

  methods:{
    currentView(){
      this.$emit('switchviewhome')
    },
  }

}
</script>

<style scoped>
/* main{
  display: flex;
  align-items: center;
  justify-content: start;
} */
</style>