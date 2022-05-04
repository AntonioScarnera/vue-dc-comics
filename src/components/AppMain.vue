<template>
  <div class="main-container">
    <div class="container">
      <span>
        Content goes here
      </span> 
    </div>
  </div>
</template>

<script>
export default {
  name: 'AppMain',

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
@import '../style/variables';
@import '../style/general';

.main-container{
  background-color: $dark;
  padding: 30px 0;
  span{
    color: white;
    font-size: $font-large;
  }
}
</style>
