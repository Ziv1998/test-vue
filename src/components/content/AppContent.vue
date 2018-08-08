<template>
  <div class="content">
    {{msg}}
  </div>
</template>
<script>
export default {
  data() {
    return {
      msg: 'content',
    }
  }
}

</script>
<style scoped lang="less">
.content {
  position: relative;
  float: right;
  margin-top: 70px;
  width: calc(100% - 260px);
}

</style>
