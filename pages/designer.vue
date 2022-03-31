<template>
  <div class="home">
    <div class="img_top">
      <img id="body_under" src="@/src/image/body.png" />
    </div>
    <ul class="list_designer">
      <router-link to="index">>About</router-link>
      <router-link to="index">>Contact</router-link>
      <router-link to="index">>Works//Reel</router-link>
    </ul>
    <div class="designer_typo">
      <p>DESIGNER</p>
    </div>
  </div>
</template>
<script></script>
<style lang="scss">
@import '@/src/css/global.scss';
.home { 
  .img_top img {
    opacity: 0;
    right: 0;
  }
  
  .designer_typo {
    color: $black;
    font-family: Monument Extended;
    font-size: 11vw;
    position: absolute;
    top: -5vh;
    p {
      padding-left: 40px;
      position: relative;
      z-index: -1;
    }
    &::before,
    &::after {
      content: '';
      display: inline-block;
      height: 90vh;
      position: absolute;
      width: 90vw;
      top: 5vh;
      margin: 5vh 5vw;
    }
    &::before {
      background: $orange;
      filter: invert(1);
      z-index: -3;
    }
    &::after {
      backdrop-filter: invert(1);
      -webkit-backdrop-filter: invert(1);
      z-index: -1;
    }
  }
  ul {
    font-size: 5em;
    z-index: -2;
  }
  .list_designer {
    font-family: Montserrat;
    bottom: 0;
    font-weight: 800;
    margin-bottom: 5vh;
  }
}
</style>
