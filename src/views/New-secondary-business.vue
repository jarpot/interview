<template>
  <div>
    <div class="main">
      <el-divider content-position="center">
        <span style="color:#4d8afe;padding:0;font-size:34px">&#10102;</span>
        <span style="vertical-align:super;margin-left:5px">协议主体</span>
      </el-divider>
      <div>
        <el-form :model="form" class="" label-width="80px">
          <el-form-item label="协议客户">
            <el-input v-model="form.user" placeholder="选择客户"></el-input>
          </el-form-item>
          <el-form-item label="协议状态">
            <el-select v-model="form.region" placeholder="正常">
              <el-option label="区域一" value="shanghai"></el-option>
              <el-option label="区域二" value="beijing"></el-option>
            </el-select>
          </el-form-item>
          <el-form-item label="购进指标">
            <el-select v-model="form.region" placeholder="金额">
              <el-option label="区域一" value="shanghai"></el-option>
              <el-option label="区域二" value="beijing"></el-option>
            </el-select>
            <el-input v-model="form.user" style="width:300px" placeholder="输入金额/数量"></el-input>
          </el-form-item>
          <el-form-item label="纯销指标">
            <el-select v-model="form.region" placeholder="金额">
              <el-option label="区域一" value="shanghai"></el-option>
              <el-option label="区域二" value="beijing"></el-option>
            </el-select>
            <el-input v-model="form.user" style="width:300px" placeholder="输入金额/数量"></el-input>
          </el-form-item>
          <el-form-item label="销售区域">
            <el-cascader :options="options" :show-all-levels="false"></el-cascader>
          </el-form-item>
          <el-form-item label="签订时间">
            <el-input style="width:50%" v-model="form.user" placeholder="2020-02-01 18:25"></el-input>
          </el-form-item>
          <el-form-item label="购进渠道">
            <el-select v-model="form.region" placeholder="指定渠道">
              <el-option label="区域一" value="shanghai"></el-option>
              <el-option label="区域二" value="beijing"></el-option>
            </el-select>
            <el-button>请选择渠道</el-button>
          </el-form-item>
          <el-table :data="tableData" style="width: 100%">
            <el-table-column prop="date" label="日期" min-width="33%">
            </el-table-column>
            <el-table-column prop="name" label="姓名" min-width="33%">
            </el-table-column>
            <el-table-column prop="address" label="地址" min-width="33%">
            </el-table-column>
          </el-table>
        </el-form>

      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      form: {
        user: "",
        region: "",
      },
      tableData: [
        {
          date: "2016-05-02",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1518 弄",
        },
        {
          date: "2016-05-04",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1517 弄",
        },
        {
          date: "2016-05-01",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1519 弄",
        },
        {
          date: "2016-05-03",
          name: "王小虎",
          address: "上海市普陀区金沙江路 1516 弄",
        },
      ],
    };
  },
  methods: {
    onSubmit() {
      console.log("submit!");
    },
  },
};
</script>
<style lang="less" scoped>
.main{
  font-size: 10px;
}
.el-form-item {
  margin-bottom: 22px;
  float: left;
  width: 50%;
  .el-form-item__content {
    display: flex;
    .el-input {
      width: 130px;
    }
  }
}
.el-divider__text {
  background-color: #e9eef3;
}
</style>