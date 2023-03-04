<template>
  <div>
    <div class="main">
      <el-divider content-position="center">
        <span style="color:#4d8afe;padding:0;font-size:34px">&#10103;</span>
        <span style="vertical-align:super;margin-left:5px">产品政策</span>
      </el-divider>
      <div>
        <div class="head">
          <el-button type="primary">主要按钮</el-button>
          <span>购进总指标（万元）：¥152.65指标按季度分解（万元）：[Q1]¥12.5，[Q2]¥12.5，[Q3]¥12.5，[Q4】¥12.5纯销总指标（万元）：¥152.65</span>
        </div>
        <div class="ban">
          <el-form :inline="true" :model="formInline" class="demo-form-inline">
            <el-form-item label="产品">
              <el-button>选择产品</el-button>
            </el-form-item>
            <el-form-item label="协议效期" style="flex:1">
              <el-col :span="11">
                <el-date-picker type="date" placeholder="选择日期" v-model="formInline.date1"></el-date-picker>
              </el-col>
            </el-form-item>
            <el-form-item>
              <el-button style="color:orange">删除</el-button>
            </el-form-item>
          </el-form>
          <div style="margin: 20px;"></div>
          <el-form label-position="top" label-width="80px" :model="formLabelAlign" style="background-color: white;">
            <el-form-item label="协议价（元）">
              <el-input v-model="formLabelAlign.name" placeholder="请输入"></el-input>
            </el-form-item>
            <el-form-item label="票折（元）">
              <el-input v-model="formLabelAlign.region" placeholder="请输入"></el-input>
            </el-form-item>
            <el-form-item label="购进指标量（大单位）">
              <el-input v-model="formLabelAlign.type" placeholder="请输入"></el-input>
            </el-form-item>
            <el-form-item label="购进指标量（小单位）">
              <el-input v-model="formLabelAlign.type" placeholder="请输入"></el-input>
            </el-form-item>
            <el-form-item label="购进金额（万元）">
              <el-input v-model="formLabelAlign.type" placeholder="请输入"></el-input>
            </el-form-item>
            <el-form-item label="纯销指标量（小单位）">
              <el-input v-model="formLabelAlign.type" placeholder="请输入"></el-input>
            </el-form-item>
            <el-form-item label="纯销指标金额（万元）">
              <el-input v-model="formLabelAlign.type" placeholder="请输入"></el-input>
            </el-form-item>
          </el-form>
          <el-form label-position="top" label-width="80px" :model="formLabelAlign" style="background-color: white;">
            <el-form-item label="分销奖励">
              <el-input v-model="formLabelAlign.name" placeholder="请输入"></el-input>
            </el-form-item>
            <el-form-item label="费用科目">
              <el-input v-model="formLabelAlign.region" placeholder="请输入"></el-input>
            </el-form-item>
            <el-form-item label="零售配送">
              <el-input v-model="formLabelAlign.type" placeholder="请输入"></el-input>
            </el-form-item>
            <el-form-item label="费用科目">
              <el-input v-model="formLabelAlign.type" placeholder="请输入"></el-input>
            </el-form-item>
            <el-form-item label="医疗配送商">
              <el-input v-model="formLabelAlign.type" placeholder="请输入"></el-input>
            </el-form-item>
            <el-form-item label="费用科目">
              <el-input v-model="formLabelAlign.type" placeholder="请输入"></el-input>
            </el-form-item>
            <el-form-item label="白定义7">
              <el-input v-model="formLabelAlign.type" placeholder="请输入"></el-input>
            </el-form-item>
            <el-form-item label="白定义8">
              <el-input v-model="formLabelAlign.type" placeholder="请输入"></el-input>
            </el-form-item>
          </el-form>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      formInline: {
        user: "",
        region: "",
        date1: "",
      },
      formLabelAlign: {
        name: "",
        region: "",
        type: "",
      },
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
.main {
  font-size: 10px;
  /deep/ .head {
    button {
      margin-right: 30px;
    }

    display: flex;
    align-items: center;
  }
  .ban {
    .demo-form-inline {
      margin-bottom: 10px;
      background-color: white;
    }
    .el-form-item {
      margin: 10px 0;
    }
    .el-form {
      display: flex;
    }
    .el-form--label-top {
        .el-form-item{
        margin: 0;
        // padding: 5px 10px;
        }
      /deep/ .el-form-item__label {
        width: 100%;
        background-color: #f8f8f8;
      }
    }
  }
}
</style>