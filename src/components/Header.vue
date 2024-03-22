<script>
  export default {
    data(){
      return{
        categories: [
          {name: 'Donna', link:'#'},
          {name: 'Uomo', link:'#'},
          {name: 'Bambino', link:'#'}
        ],
        icons: [
          {iconName: 'user', class:'fa-regular fa-user', link:'#'},
          {iconName: 'heart', class:'fa-regular fa-heart', link:'#'},
          {iconName: 'shop', class:'fa-solid fa-bag-shopping', link:'#'}
        ]

      }
    }
        
  }
</script>
<template>
  <header>
    <div class="wrapper">
      <div class="container">
        <div>
          <a v-for="(category, index) in categories" :key="`m-${index}`" :href="category.link" class="top-link">{{ category.name }}</a>
        </div>
        <div>
          <img src="/img/boolean-logo.png" alt="boolean-logo" id="logo">
        </div>
        <div class="icon">
          <a v-for="(icon, index) in icons" :key="`i.${index}`" :href="icon.link">
            <i :class="icon.class"></i>
          </a> 
        </div>
      </div>
    </div>
 </header>
</template>


<style lang="scss" scoped>
@use '../assets/scss/partials/variables' as *;

.wrapper{
  height:50px;
  background-color: $orange;
  color:white;
  font-weight: bold;
  margin-bottom: 20px;
  box-shadow: 0 1px 3px grey;
  width: 100%;
  position: fixed;
  z-index: 999;
  display: flex;
  align-items: center;
  .container{
    display: flex;
    justify-content: space-between;
    margin: 0 auto;
    div{
     width: 100px;
    }
   }
  a{
    text-decoration: none;
    color: white;
    padding: 5px;
    &:hover{
      text-decoration: underline;
    }
  }
}
#logo{
  width: 100px;
  height:24px;
}
</style>