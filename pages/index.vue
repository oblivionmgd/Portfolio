<template>
  <div class="home">
    <div class="designer_letter">
      <p>DESIGNER</p>
      <p>DESIGNER</p>
      <p>DESIGNER</p>
      <p>DESIGNER</p>
      <p>DESIGNER</p>
      <p>DESIGNER</p>
    </div>
    <div class="list_dev">
      <p>guest@Oblivion /portfolio% </p>
    </div>
    <div class="img_top">
      <img src="@/src/image/body.png" />
    </div>
    <div class="dev_letter">#Deve-<br>loper</div> 
  </div>
</template>
<script></script>
<style lang="scss">
@import '@/src/css/global.scss';
.home {
  .img_top {
    img {
      right:50%;
      transform: translateX(50%);
    }
  }
  .designer_letter {
    top: 0;
    left: 50vw;
    
    &::before,
    &::after {
      width: 45vw;
    }
  }
  .dev_letter {
    top: 50%;
    text-align: left;
    transform: translateY(-50%);
  }
  .list_dev {
    top: 0;
    left: 0;
    &::before,
    &::after {
      width: 45vw;
      top: 0;
    }
    p {
      position: absolute;
      margin: 6vh 6vw;
    }
  }
}
</style>
