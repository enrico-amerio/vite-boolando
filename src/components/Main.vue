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
    methods: {
    getDiscountValue(product) {
      const discountBadge = product.badges.find(badge => badge.type === "discount");
      return discountBadge ? discountBadge.value : "";
    },
    getSustainabilityBadge(product) {
      const sustainabilityBadge = product.badges.find(badge => badge.type === "tag");
      return sustainabilityBadge ? sustainabilityBadge.value : "";
    }
  },
};

  
</script>
<template>
  <main>
    <Card 
    v-for="(product) in products.products" :key="product.id" :product="product"
      :frontImg="`src/assets/img/${product.frontImage}`" 
      :backImg="`src/assets/img/${product.backImage}`"
      :fullPrice="product.price"
      :brand="product.brand"
      :productName="product.name"
      :discountValue="getDiscountValue(product)"
      :sustainabilityBadge="getSustainabilityBadge(product)"
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