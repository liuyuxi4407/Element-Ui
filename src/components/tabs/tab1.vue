<template>
  <div class="ta1">
    <el-tabs stretch v-model="activeName" @tab-click="handleClick">
      <el-tab-pane label="用户管理" name="first">用户管理</el-tab-pane>
      <el-tab-pane label="配置管理" name="second">配置管理</el-tab-pane>
      <el-tab-pane label="角色管理" name="third">角色管理</el-tab-pane>
      <el-tab-pane label="定时任务补偿" name="fourth">定时任务补偿</el-tab-pane>
    </el-tabs>
  </div>
</template>

<script>
export default {
  name: "Tab1",
  components: {},
  data() {
    return {
      activeName: "second",
    };
  },
  methods: {
    handleClick(tab, event) {
      console.log(tab, event);
    },
  },
};
</script>

<style >
.ta1 {
  width: 70%;
  height: 500px;
  margin: 0 auto;
  background-color: #666;
}
/* 长的下边框 */
.el-tabs__nav-wrap::after {
  /* background-color: red; */
  opacity: 0 !important;
}
/* 短的下边框 */
.el-tabs__active-bar {
  background-color: aqua !important;
}
/* 字体颜色 */
.el-tabs__item.is-active {
  color: aqua !important;
  font-size: 23px !important;
  font-weight: bold;
}
/* 未选中tab字体 */
.el-tabs__item {
  color: #fff !important;
  font-size: 23px !important;
  font-weight: bold;

}

/* .el-tabs__nav-wrap
.el-tabs__nav-scroll
.el-tabs__nav {
    width: 100%;
    display: flex;
    justify-content: space-around;
} */
</style>