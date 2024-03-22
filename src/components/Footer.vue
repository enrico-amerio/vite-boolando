<script>
  export default {
    data(){
      return{
        links:[
          {name:'Informazioni legali', link:'#'},
          {name:'Informativa sulla privacy', link:'#'},
          {name:'Diritto di recesso', link:'#'}
        ],
        socials:[
          {name:'Twitter', class:'fa-brands fa-square-twitter', link:'#'},
          {name:'Facebook', class:'fa-brands fa-square-facebook', link:'#'},
          {name:'Instagram', class:'fa-brands fa-square-instagram', link:'#'},
          {name:'Pinterest', class:'fa-brands fa-square-pinterest', link:'#'},
          {name:'Youtube', class:'fa-brands fa-square-youtube', link:'#'}
        ]
      }
    }
  }
</script>
<template>
  <footer>
    <div class="container">
      <div>
        <h6>Boolando s.r.l</h6>
        <div>
          <a v-for="(link, index) in links" :key="index" href="#">{{link.name}}</a>
        </div>
      </div>
      <div>
        <h6>Trovaci anche su</h6>
        <div>
          <a v-for="(social, index) in socials" :key='index' :href="social.link">
            <i :class="social.class"></i>
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>


<style lang="scss" scoped>
footer{
  background-color: black;
  height: 60px;
  color: white;
  display: flex;
  z-index: 999;
  .container{
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 0 auto;
    a{
      text-decoration: none;
      color: white;
      font-size: x-small;
      margin-right: 5px;
      &:hover{
        text-decoration: underline;
      }
    }
  }
}
</style>