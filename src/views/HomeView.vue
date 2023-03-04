<template>
  <div class="home">
    <el-container>
      <el-aside width="200px">
        <div><img src="../../public/imgs/1.png" width="100%" alt=""></div>
        <el-menu :default-openeds="['1', '3']">
          <el-submenu index="1">
            <template slot="title"><i class="el-icon-message"></i>导航一</template>
            <el-menu-item-group>
              <el-menu-item index="1-1">选项1</el-menu-item>
              <el-menu-item index="1-2">选项2</el-menu-item>
              <el-menu-item index="1-3">选项3</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
          <el-submenu index="2">
            <template slot="title"><i class="el-icon-menu"></i>导航二</template>
            <el-menu-item-group>
              <el-menu-item index="2-1">选项1</el-menu-item>
              <el-menu-item index="2-2">选项2</el-menu-item>
              <el-menu-item index="2-3">选项3</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
          <el-submenu index="3">
            <template slot="title"><i class="el-icon-setting"></i>导航三</template>
            <el-menu-item-group>
              <el-menu-item index="3-1">选项1</el-menu-item>
              <el-menu-item index="3-2">选项2</el-menu-item>
              <el-menu-item index="3-3">选项3</el-menu-item>
            </el-menu-item-group>
          </el-submenu>
        </el-menu>
      </el-aside>
      <el-container>
        <el-header>
          <headerVue></headerVue>
        </el-header>
        <el-main>
          <Crumbs></Crumbs>
          <NewSecondaryBusiness></NewSecondaryBusiness>
          <ProductPolicy></ProductPolicy>
          <More></More>
        </el-main>
        <div class="footer">
          <el-button type="primary">保存</el-button>
        </div>
      </el-container>

    </el-container>
  </div>
</template>

<script>
import More from "./more";
import ProductPolicy from "./Product-policy";
import NewSecondaryBusiness from "./New-secondary-business";
import Crumbs from "@/components/crumbs";
import headerVue from "@/components/header.vue";

export default {
  name: "HomeView",
  components: {
    More,
    ProductPolicy,
    NewSecondaryBusiness,
    Crumbs,
    headerVue,
  },
};
</script>
<style lang="less" scoped>
body {
  margin: 0;
  padding: 0;
}
.el-header {
  background-color: #2a3139;
  color: #c2c1bf;
  text-align: center;
  line-height: 60px;
}

.el-aside {
  background-color: #293038;
  color: white;
  text-align: center;
  // height: 100vh;

  /deep/ .el-menu {
    background-color: #293038;
    color: white;
    /deep/ .el-submenu__title {
      color: white;
    }
    .el-menu-item {
      color: white;
    }
  }
}

.el-main {
  background-color: #e9eef3;
  color: #333;
  line-height: 100%;
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