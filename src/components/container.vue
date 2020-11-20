<template>
  <div class="contenters">
    <el-container>
      <el-header>Header</el-header>

      <el-container>
        <el-aside>Adise</el-aside>
        <el-main>
          <el-row>
            <el-col :span="24">
              <div class="grid-content bg-purple-light">
                <i class="el-icon-edit"></i>
                <div class="el-icon-delete-solid">垃圾箱</div>
              </div>
            </el-col>
          </el-row>
        </el-main>
      </el-container>

      <el-footer>Footer</el-footer>
    </el-container>
  </div>
</template>

<script>
export default {
  name: "contenters",
};
</script>

<style lang="less" scoped>
.bg-purple-light {
  background: #e5e9f2;
  font-size: 40px;
}
.grid-content {
  border-radius: 4px;
  min-height: 460px;
}
.el-header,
.el-footer {
  background-color: #b3c0d1;
  color: #333;
  text-align: center;
  line-height: 60px;
}

.el-aside {
  background-color: #d3dce6;
  color: #333;
  text-align: center;
  line-height: 200px;
}

.el-main {
  background-color: #e9eef3;
  color: #333;
  text-align: center;
  line-height: 160px;
}

body > .el-container {
  margin-bottom: 40px;
}

.el-container:nth-child(5) .el-aside,
.el-container:nth-child(6) .el-aside {
  line-height: 260px;
}

.el-container:nth-child(7) .el-aside {
  line-height: 320px;
}
</style>