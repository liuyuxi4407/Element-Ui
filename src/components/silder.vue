<template>
  <div class="silder">
    <div class="block">
      <span class="demonstration">默认</span>
      <el-slider v-model="value1"></el-slider>
    </div>
    <div class="block">
      <span class="demonstration">自定义初始值</span>
      <el-slider v-model="value2"></el-slider>
    </div>
    <div class="block">
      <span class="demonstration">隐藏 Tooltip</span>
      <el-slider v-model="value3" :show-tooltip="false"></el-slider>
    </div>
    <div class="block">
      <span class="demonstration">格式化 Tooltip</span>
      <el-slider v-model="value4" :format-tooltip="formatTooltip"></el-slider>
    </div>
    <div class="block">
      <span class="demonstration">禁用</span>
      <el-slider v-model="value5" disabled></el-slider>
    </div>

    <div class="block">
      <el-slider v-model="value" vertical height="200px"> </el-slider>
    </div>
     <el-alert
    title="成功提示的文案"
    type="success">
  </el-alert>
  </div>
  
</template>

<script>
export default {
  name: "silder",
  data() {
    return {
      value: 0,
      value1: 0,
      value2: 50,
      value3: 36,
      value4: 48,
      value5: 42,
    };
  },
  methods: {
    formatTooltip(val) {
      return val / 100;
    },
  },
};
</script>

<style lang="less">
</style>






