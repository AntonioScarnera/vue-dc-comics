<template>
  <div>

    <footer-head/>
    <div>

    </div>
    <div class="footer-bottom">
      <div class="container d-flex justify-content-between align-items-center footer-bottom-container">

        <div class="signup">SIGN-UP NOW!</div>
        <div class="socials d-flex align-items-center">
          <span>FOLLOW US</span>
          <ul>
            <li v-for="(item, index) in socials" :key="index">
              <img :src="item.url" alt="">
            </li>
          </ul>
        </div>
      </div>
    </div>

  </div>
</template>

<script>
import FooterHead from './FooterHead.vue'
export default {
  name: 'AppFooter',
  components:{
    FooterHead
  },
  data(){
    return{
      socials:[
        {
          url: require('../assets/images/footer-facebook.png')
        },
        {
          url: require('../assets/images/footer-twitter.png')
        },
        {
          url: require('../assets/images/footer-youtube.png')
        },
        {
          url: require('../assets/images/footer-pinterest.png')
        },
        {
          url: require('../assets/images/footer-periscope.png')
        },
        ]
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/variables';
@import '../style/general';

.footer-bottom{
  height: 85px;
  background-color: rgb(51, 51, 51);
}
.footer-bottom-container{
  height: 100%;
}
.signup{
  font-size: $font-small;
  color: white;
  padding: 12px;
  border: 2px solid $color-azzurro;
}

.socials{

  gap: 15px;
  color: $color-azzurro;
  font-weight: 600;
  font-size: $font-medium;

  ul{
    li{
      list-style: none;
      display: inline-block;
      margin: 0 6px;

      img{
        width: 30px;
      }
    }
  }
}
</style>
