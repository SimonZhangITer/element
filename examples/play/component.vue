<template>
<div>
  <el-button @click="value = '#fff'">Change Value</el-button>
  <div>Value: {{ value }}</div>
  <el-color-picker v-model="value"></el-color-picker>
  <div>Value2: {{ value2 }}</div>
  <el-color-picker v-model="value2" show-alpha></el-color-picker>
  <el-table :data="tableData" style="width: 100%" ref="table">
    <el-table-column prop="date" label="日期" width="180" label-class-name="test">
    </el-table-column>
    <el-table-column prop="name" label="姓名" width="180">
    </el-table-column>
    <el-table-column prop="address" label="地址">
    </el-table-column>
  </el-table>
</div>

</template>

<style>
.test {
  background: red!important;
  color: white!important
}

</style>

<script type="text/ecmascript-6">
export default {
  created() {
    window.x = this;
  },
  data() {
    return {
      value: '#bfcbd9',
      value2: null,
      tableData: [{
        date: '2016-05-02',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1518 弄1'
      }, {
        date: '2016-05-04',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1517 弄'
      }, {
        date: '2016-05-01',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1519 弄'
      }, {
        date: '2016-05-03',
        name: '王小虎',
        address: '上海市普陀区金沙江路 1516 弄'
      }]
    };
  }
};

</script>
