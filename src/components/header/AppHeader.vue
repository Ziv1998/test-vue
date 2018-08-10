<template>
  <div class="header">
    <div class="logo">
      <img src="../../assets/logo.png">
      <p>{{company_name}}</p>
    </div>
    <!-- <div class="menu-btn">
      <i class="fa fa-list"></i>
    </div> -->
  </div>
</template>
<script>
export default {
  data() {
    return {
      company_name: '深圳市思维树科技有限公司',
    }
  }
}

</script>
<style scoped lang="less">
.header {
  position: fixed;
  left: 0px;
  right: 0px;
  background-color: #FFFFFF;
  overflow: hidden;
  z-index: 999;
  height: 60px;
  .logo {
    float: left;
    height: 100%;
    // @media (max-width: 768px) {
    //   display: none;
    // }
    img {
      margin: 10px 0px;
      height: 40px;
      float: left;
    }
    p {
      float: left;
      font-size: 18px;
      font-weight: 600;
    }
  }
  // .menu-btn{
  //   float: left;
  //   display: none;
  //   padding: 15px 10px;
  //   cursor: pointer;
  //   margin-left: 20px;
  //   @media (max-width: 768px) {
  //     display: block;
  //   }
  //   i{
  //     font-size: 30px;
  //   }
  // }
  // .menu-btn:hover{
  //   color:#00AAFF;
  // }
}

</style>
