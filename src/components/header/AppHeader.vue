<template>
  <div class="header">
    <div class="logo">
      <img src="../../assets/logo.png">
      <h2>{{company_name}}</h2>
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
	padding: 0px 15px;
	background-color: #FFFFFF;
	overflow: hidden;
	z-index: 999;
  .logo {
  	padding: 0px 10px;
    float: left;
    height: 100%;
    img {
      margin: 5px 0px;
      height: 60px;
      float: left;
    }
    h2 {
      float: left;
      margin-left: 10px;
    }
  }
}

</style>
