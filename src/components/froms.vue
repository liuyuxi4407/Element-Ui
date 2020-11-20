<template>
  <div class="froms">
    <el-radio v-model="radio" label="3">是</el-radio>
    <el-radio v-model="radio" label="2">不是</el-radio>
    <br />
    <el-checkbox v-model="checked">北京</el-checkbox>

    <!-- <el-checkbox-group v-model="checkList">
      <el-checkbox label="复选框 A"></el-checkbox>
      <el-checkbox label="复选框 B"></el-checkbox>
      <el-checkbox label="复选框 C"></el-checkbox>
      <el-checkbox label="禁用" disabled></el-checkbox>
      <el-checkbox label="选中且禁用" disabled></el-checkbox>
    </el-checkbox-group> -->
    <br/>
    <el-checkbox
      :indeterminate="isIndeterminate"
      v-model="checkAll"
      @change="handleCheckAllChange"
      >全选</el-checkbox
    >
    <div style="margin: 15px 0"></div>
    <el-checkbox-group
      v-model="checkedCities"
      @change="handleCheckedCitiesChange"
    >
      <el-checkbox v-for="city in cities" :label="city" :key="city">{{
        city
      }}</el-checkbox>
    </el-checkbox-group>

     <el-input-number v-model="num" @change="handleChange" :min="1" :max="10" label="描述文字"  controls-position="right"></el-input-number>
     
  </div>
</template>
<script>
const cityOptions = ['上海', '北京', '广州', '深圳'];

export default {
  name: "froms",
  data() {
    return {
        num: 1,
      radio: "3",
      checked: false,
      //   checkList: ["选中且禁用", "复选框 A"],
      checkAll: false,
      checkedCities: ["上海", "北京"],
      cities: cityOptions,
      isIndeterminate: true,
    };
  },
  create: {

  },
  methods: {
    handleCheckAllChange(val) {
      this.checkedCities = val ? cityOptions : [];
      this.isIndeterminate = false;
    },
    handleCheckedCitiesChange(value) {
      let checkedCount = value.length;
      this.checkAll = checkedCount === this.cities.length;
      this.isIndeterminate =
        checkedCount > 0 && checkedCount < this.cities.length;
    },
    handleChange(v) {
        console.log(v)
    }
  },
};
</script>
<style lang="less">
</style>
