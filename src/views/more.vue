<template>
  <div>
    <div class="more-head">
      <el-divider content-position="center">
        <span style="color:#4d8afe;padding:0;font-size:34px">&#10103;</span>
        <span style="vertical-align:super;margin-left:5px">补充协议</span>
      </el-divider>
    </div>
    <div class="main">
      <div style="margin-bottom: 20px;z-index: 999;position: absolute;right: 30px;">
        <el-button size="small" @click="addTab(editableTabsValue)">
          add tab
        </el-button>
      </div>
      <el-tabs v-model="editableTabsValue" type="card" closable @tab-remove="removeTab">
        <el-tab-pane v-for="(item, index) in editableTabs" :key="index" :label="item.title" :name="item.name">
          <div>协议内容</div>
          <el-input type="textarea" :rows="5" placeholder="请输入内容" v-model="textarea">
          </el-input>
        </el-tab-pane>
      </el-tabs>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      editableTabsValue: "2",
      editableTabs: [
        {
          title: "Tab 1",
          name: "1",
          content: "Tab 1 content",
        },
        {
          title: "Tab 2",
          name: "2",
          content: "Tab 2 content",
        },
      ],
      tabIndex: 2,
    };
  },
  methods: {
    addTab(targetName) {
      let newTabName = ++this.tabIndex + "";
      this.editableTabs.push({
        title: "New Tab",
        name: newTabName,
        content: "New Tab content",
      });
      this.editableTabsValue = newTabName;
    },
    removeTab(targetName) {
      let tabs = this.editableTabs;
      let activeName = this.editableTabsValue;
      if (activeName === targetName) {
        tabs.forEach((tab, index) => {
          if (tab.name === targetName) {
            let nextTab = tabs[index + 1] || tabs[index - 1];
            if (nextTab) {
              activeName = nextTab.name;
            }
          }
        });
      }

      this.editableTabsValue = activeName;
      this.editableTabs = tabs.filter((tab) => tab.name !== targetName);
    },
  },
};
</script>
<style lang="less" scoped>
.main {
  /deep/ .el-tabs__item {
    background-color: white;
  }
  /deep/ .el-tabs__content {
    padding: 5px;
    background-color: white;
  }
}
</style>