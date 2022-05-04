<template>
  <div class="container d-flex justify-content-between align-items-center header-container">
    <div class="logo">
      <img src="../assets/images/dc-logo.png" alt="">
    </div>
    <nav>
      <ul>
        <li v-for="(item, index) in links" :key="index" :class="{'selected': item.active}" @click="clicca(index)">
          <a :class="{'active': item.active}">{{item.nome.toUpperCase()}}</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'AppHeader',
  data(){
    return{
      links:[
        {
          nome: 'characters',
          link:'',
          active: false
        },
        {
          nome: 'comics',
          link:'',
          active: false
        },
        {
          nome: 'movies',
          link:'',
          active: false
        },
        {
          nome: 'tv',
          link:'',
          active: false
        },
        {
          nome: 'games',
          link:'',
          active: false
        },
        {
          nome: 'collectibles',
          link:'',
          active: false
        },
        {
          nome: 'videos',
          link:'',
          active: false
        },
        {
          nome: 'fans',
          link:'',
          active: false
        },
        {
          nome: 'news',
          link:'',
          active: false
        },
        {
          nome: 'shop',
          link:'',
          active: false
        },
      ]
    }
  },
  methods:{
    clicca(i){
      if(this.links[i].active === true)
      {
        this.links[i].active = false;
      }
      else{
        this.links[i].active = true;
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/variables';
@import '../style/general';

.selected{
  border-bottom: 4px solid $color-azzurro;
}
.active{
  color: $color-azzurro;
}


.header-container{ 
  height: 90px;
  min-width: 992px;

  .logo{

    img{
      width: 60px;
    }
  }

  nav{
    
    ul{
      

      li{
        display: inline-block;
        list-style: none;
        height: 90px;
        line-height: 90px;
        

        a{
          font-size: $font-small;
          padding: 38px 10px;
          text-decoration: none;
          font-weight: 600;
          cursor: pointer;

          &:hover{
            color: $color-azzurro;
          }
        }

        &:hover{
          border-bottom: 4px solid $color-azzurro;
          
        }
      }
    }

  }
}
</style>
