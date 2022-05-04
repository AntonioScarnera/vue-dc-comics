<template>
  <div>

    <footer-head/>
    
    <div class="footer-main">
      <div class="container d-flex justify-content-between align-items-center">
        <div class="d-flex link-list">

          <div class="link-container">
            <span>DC COMICS</span>
            <ul>
              <li>Characters</li>
              <li>Comics</li>
              <li>Movies</li>
              <li>TV</li>
              <li>Games</li>
              <li>Videos</li>
              <li>News</li>
            </ul>
              <br><br>
            <span>SHOP</span>
            <ul>
              <li>Shop DC</li>
              <li>Shop DC Collectibles</li>
            </ul>
          </div>

          <div class="link-container">
            <span>DC</span>
            <ul>
              <li>Terms Of Use</li>
              <li>Privacy policy (New)</li>
              <li>Ad Choice</li>
              <li>Advertising</li>
              <li>Jobs</li>
              <li>Subscription</li>
              <li>Talent Workshop</li>
              <li>CPSC Certificates</li>
              <li>Rating</li>
              <li>Shop Help</li>
              <li>Contact Us</li>
            </ul>
          </div>

          <div class="link-container">
            <span>SITES</span>
            <ul>
              <li>DC</li>
              <li>MAD Magazine</li>
              <li>DC Kids</li>
              <li>DC Universe</li>
              <li>DC Power Visa</li>
            </ul>
          </div>

        </div>

        <div class="big-logo">
          <img src="../assets/images/dc-logo-bg.png">
        </div>
      </div>      
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
  min-width: 992px;
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


.footer-main{
  background-image: url(../assets/images/footer-bg.jpg);
  background-size: cover;
  min-width: 992px;
  .link-list{
    padding: 30px;

    .link-container{
      padding: 20px;

      span{
        color: white;
        font-size: $font-large;
      }

      ul{
        padding-top: 12px;
        li{
          list-style: none;
          padding: 5px 0;
          color: grey;
        }
      }
    }
  }

  .big-logo{
    img{
      width: 500px;
      }
  }
}
</style>
