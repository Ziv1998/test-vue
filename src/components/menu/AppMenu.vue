<template>
  <div class="menu">
    <ul>
      <li v-for="(arr,index) in data">
        <a href="#" :class="{ active:arr.active }">
          <i v-bind:class="'fa fa-'+arr.icon"></i>
          <span>{{arr.text}}</span>
        </a>
      </li>
    </ul>
  </div>
</template>
<script>
export default {
  data() {
    return {
      data: [{
        icon: "home",
        text: "设备列表",
        active: true
      }, {
        icon: "coffee",
        text: "维修记录",
        active: false
      }, {
        icon: "coffee",
        text: "维修记录",
        active: false
      }, {
        icon: "coffee",
        text: "维修记录",
        active: false
      }, {
        icon: "coffee",
        text: "维修记录",
        active: false
      }]
    }
  },
  methods: {
    overShow(i) {
      this.data[i].active = true;
    },
    outHide(i) {
      this.data[i].active = false;
    }
  }
}

</script>
<style scoped lang="less">
.menu {
  position: fixed;
  left: 0px;
  float: left;
  margin-top: 60px;
  width: 260px;
  height: 100%;
  background-color: #2B333E;
  ul {
    list-style: none;
    padding-left: 0px;
    margin: 0px;
    li {
      a {
        display: block;
        border-left: 5px solid transparent;
        padding: 18px 30px;
        color: #AEB7C2;
        text-align: left;
        span {
          margin-left: 10px;
          transition: all 0.3s ease-in-out;
        }
      }
    }
    .active,
    a:hover {
      color: #00AAFF;
      span {
        color: #FFFFFF;
      }
    }
    .active{
      background-color: #252c35;
      border-left-color: #00AAFF;
    }
  }
}

</style>
