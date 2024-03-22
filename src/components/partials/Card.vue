    <script>
      export default {
        props:{
          frontImg: String,
          backImg: String
        },
        mounted(){
          console.log(this.frontImg);
        }
      }
    </script>

<template>
  <div class="card">
    <div class="card-img-container" >
      <img :src="frontImg" alt="1" class="img-a">
      <img :src="backImg" alt="1b" class="img-b">
      <span class="hearts">&hearts;</span>
      <span class="sale">-50&percnt;</span>
      <span class="sustain">Sostenibilità</span>
    </div>
    <div class="caption">
      <h5>Levi's</h5>
      <h3>TEE UNISEX</h3>
      <span class="price">14,99 &euro;</span><span class="full-price">29,99&euro;</span>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card-img-container{
  width: 335px;
  height: 480px;
  margin:7px;
  position:relative;
  .img-a, .img-b{
  max-width: 335px;
  max-height: 485px;
  position: absolute;
}
  .img-a{
    z-index: 1;
    &:hover{
      display: none;
    }
  }
  .sustain, .sale{
    z-index: 1;
    padding:7px;
    color: white;
    font-size: 10px;
    font-weight: bold;
    position: relative;
    top: 425px;
  }
  .sustain{
    background-color: green;
  }
  .sale{
    background-color: red;
  }
  .hearts{
    position:absolute;
    top: 7px;
    right: 0px;
    z-index:1;
    background-color: white;
    padding: 2px 10px;
    font-size: 30px;
  }
}
.caption{
  margin-bottom: 10px;
  padding-left: 7px;
  h5{
    font-weight: 400;
  }
  .price {
  color: red;
  font-weight: bold;
  }
  .full-price{
    text-decoration: line-through;
  }
}
</style>