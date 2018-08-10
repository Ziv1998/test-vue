<template>
  <div id="menu-content">
    <div class="left-menu" ref="left_menu">
      <ul>
        <li v-for="(arr,index) in data">
          <a href="#" :class="{ active:arr.active,collapsed:arr.child&&!arr.active }" @click="menu_click(index,$event)">
            <i v-bind:class="'fa fa-'+arr.icon"></i>
            <span>{{arr.text}}</span>
            <i v-if="arr.child" class="icon-submenu fa fa-angle-right"></i>
          </a>
        </li>
      </ul>
    </div>
    <div class="right-content" ref="right_content">
      <div class="menu-btn" :class="{ close:menuState }" @click="menu_btn">
        <i class="fa fa-arrow-circle-o-right"></i>
      </div>
      <component v-bind:is="currentTabComponent"></component>
    </div>
  </div>
</template>
<script>
import AppContent from '../content/AppContent.vue';
import ContentTest1 from '../content/ContentTest1.vue';
import ContentTest2 from '../content/ContentTest2.vue';
export default {
  name: "menu-content",
  components: {
    AppContent,
    ContentTest1,
    ContentTest2
  },
  data() {
    return {
      data: [{
          icon: "home",
          tab: "AppContent",
          text: "设备列表",
          active: true
        }, {
          icon: "coffee",
          tab: "ContentTest1",
          text: "维修记录",
          active: false
        },
        // {
        //   icon: "user",
        //   text: "人员信息",
        //   active: false,
        //   child: [{
        //     text: "child1"
        //   }, {
        //     text: "child2"
        //   }, {
        //     text: "child3"
        //   }]
        // }, 
        {
          icon: "map",
          tab: "ContentTest2",
          text: "地图",
          active: false
        }
      ],
      currentTab: "AppContent",
      menuState: false,
    }
  },
  methods: {
    menu_click(i, event) {
      console.log(event.currentTarget.className)
      if (event.currentTarget.className == "collapsed") {
        this.data[i].active = true;
      } else {
        for (var m = 0; m < this.data.length; m++) {
          this.data[m].active = false;
        }
        this.data[i].active = true;
        this.currentTab = this.data[i].tab;
      }
    },
    menu_btn() {
    }
  },
  computed: {
    currentTabComponent: function() {
      return this.currentTab
    }
  }
}

</script>
<style scoped lang="less">
#menu-content {
  overflow: hidden;
}

.left-menu {
  position: fixed;
  left: 0px;
  float: left;
  margin-top: 60px;
  width: 260px;
  height: 100%;
  transition: all 0.3s ease-in-out;
  @media (max-width: 768px) {
    left: -260px;
  }
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
      .active,
      a:hover {
        color: #00AAFF;
        span {
          color: #FFFFFF;
        }
      }
      .icon-submenu {
        font-size: 20px;
        float: right;
      }
      .active {
        background-color: #252c35;
        border-left-color: #00AAFF;
        .icon-submenu {
          transition: all 0.2s ease-out;
          transform: rotate(90deg);
        }
      }
      .collapsed {
        .icon-submenu {
          transform: rotate(0deg);
        }
      }
    }
  }
}

.right-content {
  position: relative;
  float: right;
  margin-top: 60px;
  width: calc(100% - 320px);
  transition: all 0.3s ease-in-out;
  padding: 30px;
  @media (max-width: 768px) {
    width: calc(100% - 60px);
  }
  .menu-btn {
    position: absolute;
    top: 5px;
    left: 5px;
    cursor: pointer;
    font-size: 30px;
    transition: all 0.3s ease-in-out;
    transform: rotate(0deg);
    @media (min-width: 768px) {
      display: none;
    }
  }
  .menu-btn.close {
    transform: rotate(180deg);
  }
}

</style>
