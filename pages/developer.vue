<template>
  <div class="main">
    <div class="home">
      <div class="designer_hover_area"></div>
      <div class="dev_hover_area"></div>
      <div class="img_top">
        <img src="@/src/image/body.png" />
      </div>
      <div class="dev_letter">
        <p>#Developer</p>
      </div>
      <ul class="list_dev">
        <p>guest@OblivionMGD Portfolio % ls -l</p>
        <router-link to="about"
          >drwxr-xr-x oblivion staff 1024 May 14 2021 repository</router-link
        >
        <router-link to="about"
          >-rwxr-xr-x oblivion staff 4096 May 14 2021 contact.md</router-link
        >
        <router-link to="about"
          >-rwxr-xr-x oblivion staff 4096 May 14 2021 README.md</router-link
        >
        <p>guest@OblivionMGD Portfolio %</p>
      </ul>
    </div>
  </div>
</template>
<script></script>
<style lang="scss">
@import '@/src/css/global.scss';
.home {
  img_top {
    display: block;
    height: 100vh;
  }
    img {
      height: 100vh;
      right: 150%;
      position: absolute;
      transform: translateX(50%);
    }
  .dev_letter {
    color: $black;
    font-family: Noto Sans JP;
    font-size: 11vw;
    position: absolute;
    bottom: -5vh;
    right: 40px;
    &::before,
    &::after {
      content: '';
      display: inline-block;
      height: 90vh;
      position: absolute;
      width: 90vw;
      bottom: 5vh;
      right: -2.5vw;
      margin: 5vh 5vw;
    }
    &::before {
      background: $blue;
      filter: invert(1);
      z-index: -2;
    }
    &::after {
      -webkit-backdrop-filter: invert(1);
      backdrop-filter: invert(1);
    }
  }
  .dev_letter p {
    z-index: 0;
  }
  ul {
    position: absolute;
    display: grid;
    font-size: 5vh;
    list-style-type: none;
    pointer-events: auto;
    margin-block-start: 0;
    padding: 0;
  }
  .list_dev {
    font-size: 4vh;
    font-family: Courier New;
    font-weight: bold;
    text-align: left;
    left: 6vw;
    top: 4vw;
    color: $white;
    
    a {
      color: $white; 
      &::before,
      &::after {
        content: '';
        position: absolute;
        display: inline-block;
        width: 0%;
        height: 15%;
        left: 0;
        transition: width 0.7s cubic-bezier(0, 0.7, 0.5, 1),
        transform 0.7s cubic-bezier(0, 0.7, 0.5, 1);
      }
      &::before {
        background: $black;
        -webkit-filter: invert(1);
        filter: invert(1);
        z-index: -1;
      }
      &::after {
        -webkit-backdrop-filter: invert(1);
        backdrop-filter: invert(1);
      } 
      &:hover::before,
      &:hover::after {
        width: 100%;
      } 
    }
  }
}
</style>
