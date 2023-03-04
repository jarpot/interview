<template>
  <div class="header">
    <div class="header_item" v-for="(item,index) in header" :key="index">
      <i :class="item.icon"></i>
      <div>{{item.title}}</div>
    </div>
    <img src="../../public/imgs/2.png" alt="">
  </div>
</template>
<script>
export default {
  //   name: 'Header',
  data() {
    return {
      header: [
        {
          icon: "el-icon-s-home",
          title: "首页",
        },
        {
          icon: "el-icon-cloudy",
          title: "主数据",
        },
        {
          icon: "el-icon-share",
          title: "辖区管理",
        },
      ],
    };
  },
};
</script>
<style lang="less">
.header {
  display: flex;
  .header_item {
    display: flex;
    align-items: center;
    margin-right: 30px;
  }
}
</style>