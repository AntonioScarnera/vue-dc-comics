<template>
  <div class="footerHead-container">
      <div class="container">
        <ul class="d-flex justify-content-around align-items-center">
            <li v-for="(item, index) in items" :key="index">
                <div class="d-flex align-items-center">
                    <img :src="item.url">
                    <span>{{item.nome.toUpperCase()}}</span>
                    
                </div>
            </li>
        </ul>
      </div>

  </div>
</template>

<script>
export default {
  name: 'FooterHead',
  data(){
    return{
      items:[
        {
          nome: 'characters',
          url: require('../assets/images/buy-comics-digital-comics.png')
        },
        {
          nome: 'comics',
          url:require('../assets/images/buy-comics-merchandise.png')
        },
        {
          nome: 'movies',
          url:require('../assets/images/buy-comics-shop-locator.png')
        },
        {
          nome: 'tv',
          url:require('../assets/images/buy-comics-subscriptions.png')
        },
        {
          nome: 'games',
          url:require('../assets/images/buy-dc-power-visa.svg')
        }
      ]
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/variables';
@import '../style/general';

.footerHead-container{
    background-color: $color-azzurro;
    color: white;
      min-width: 992px;
        ul{
            padding: 40px 0;
            list-style: none;

            li{

                img{
                    width: 40px;
                    height: 50px;
                    margin-right: 10px;

                    &:hover{
                        cursor: pointer;
                    }

                }
                span{
                  font-size: $font-small;
                  &:hover{
                        cursor: pointer;
                    }
                }
                
            }
        }
    
}
</style>