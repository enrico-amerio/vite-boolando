<script>
import Card from './partials/Card.vue';
  export default {
        components:{
          Card
        }
  }
</script>
<template>
  <main>
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
    <Card />
  </main>
</template>


<style lang="scss" scoped>
  main{
    display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding-top: 60px;
  }
//   main{
//   display: flex;
//   flex-wrap: wrap;
//   justify-content: center;
//   padding-top: 100px;
  
// }
</style>