<template>
  <div class="header">
    <div class="logo">
      <img src="../../assets/logo.png">
      <p>{{company_name}}</p>
    </div>
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
  .logo {
    float: left;
    height: 100%;
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
}

</style>
