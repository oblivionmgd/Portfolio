<template>
  <div class="main">
    <div class="home">
      <div class="designer_hover_area"></div>
      <div class="coder_hover_area"></div>
      <div class="img_top">
        <img id="body_under" src="@/src/image/body.png" />
      </div>
      <img id="logo" src="@/src/image/logo.svg" />
      <ul class="list_designer">
        <router-link to="about">>About</router-link>
        <router-link to="about">>Contact</router-link>
        <router-link to="about">>Works//Reel</router-link>
      </ul>
      <div class="designer_typo">
        <p>DESIGNER</p>
      </div>
    </div>
  </div>
</template>
<script></script>
<style lang="scss">
@import '@/src/css/global.scss';
.home {
  overflow: hidden;
  position: relative;
  pointer-events: none;
  .img_top {
    display: block;
    height: 100vh;
  }
  img#logo {
    position: absolute;
    margin: 0vh 5vw;
    top: -10vh;
    height: 120vh;
    z-index: -2;
  }
  .img_top img {
    height: 100vh;
    right: 35%;
    position: absolute;
    transform: translateX(50%);
  }
  .designer_typo::before,
  .designer_typo::after {
    content: '';
    display: inline-block;
    height: 90vh;
    margin: 5vh 5vw;
    position: absolute;
    width: 90vw;
    top: 0;
    left: 0;
  }
  .designer_typo::before {
    background: $orange;
    filter: invert(1);
    z-index: -3;
  }
  .designer_typo::after {
    backdrop-filter: invert(1);
    -webkit-backdrop-filter: invert(1);
    z-index: -1;
  }
  .designer_typo {
    color: $black;
    font-family: Monument Extended;
    font-size: 11vw;
    position: absolute;
    top: 0;
    padding-left: 40px;
  }
  .designer_typo p {
    position: relative;
    z-index: -1;
  }
  ul {
    position: absolute;
    display: grid;
    font-size: 5vh;
    list-style-type: none;
    pointer-events: auto;
    z-index: -2;
  }
  .list_designer {
    font-family: Montserrat;
    bottom: 0;
    font-weight: 800;
    margin-bottom: 5vh;
  }
  [class*='hover_area'] {
    height: 100vh;
    width: 30vw;
    position: absolute;
    top: 0;
    pointer-events: auto;
  }
}
</style>
