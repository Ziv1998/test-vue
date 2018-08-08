<template>
  <div class="menu">
    {{msg}}
  </div>
</template>
<script>
export default {
  data() {
    return {
      msg: 'menu',
    }
  }
}

</script>
<style scoped lang="less">
.menu {
  position: fixed;
  left: 0px;
  float: left;
  margin-top: 70px;
  width: 260px;
  height: 100%;
  background-color: #2B333E;
}

</style>
