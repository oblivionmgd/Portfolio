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
      <p>guest@OblivionMGD Portfolio % </p>
    </div>
    <div class="img_top">
      <img src="@/src/image/body.png" />
    </div>
    <div class="dev_letter">#Devel<br>oper</div>
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
    
    &::before,
    &::after {
      width: 45vw;
    }
  }
  .dev_letter {
    top: 50%;
    right: 0;
    text-align: right;
    transform: translateY(-50%);
  }
  .list_dev {
    top: 0;
    right: 0; 
    &::before,
    &::after {
      width: 45vw;
      right: 0vw;
    }
    p {
      position: absolute;
      margin: 6vh 6vw;
      right: 0;
    }
  }
}
</style>
