<script>
import Card from './partials/Card.vue';
import products from '../assets/data/db.json';
export default {
    data(){
      return{
        products
      }
    },
    components:{
      Card
    },
    // mounted(){
    //   console.log(products);
    // }

  }
</script>
<template>
  <main>
    <Card 
    v-for="(product) in products.products" :key="product.id" :product="product"
      :frontImg="`src/assets/img/${product.frontImage}`" 
      :backImg="`src/assets/img/${product.backImage}`"
      />
   
  </main>
</template>


<style lang="scss" scoped>
  main{
    display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding-top: 60px;
  }
</style>