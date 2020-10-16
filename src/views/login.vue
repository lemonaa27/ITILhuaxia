<template>
  <div class="itil_papper">
    <div class="itil_head">
      <el-button>从草稿中载入</el-button>
      <el-button>保存为草稿</el-button>
    </div>
    <div>
      <el-tabs v-model="activeName" type="card" @tab-click="handleClick">
        <el-tab-pane label="用户管理" name="first">用户管理</el-tab-pane>
        <el-tab-pane label="配置管理" name="second">配置管理</el-tab-pane>
        <el-tab-pane label="角色管理" name="third">角色管理</el-tab-pane>
        <el-tab-pane label="定时任务补偿" name="fourth">定时任务补偿</el-tab-pane>
      </el-tabs>
    </div>
    <tablecell></tablecell>
    <div>

    </div>
  </div>
</template>

<script>
import tablecell from '../components/tableCommon/index'
export default {
  components: {
    tablecell
  },
  name: "",
  data() {
    return {
       activeName: 'zero'
    };
  },
  watch: {
   
  },
  created() {
    
  },
  methods: {
    handleClick(tab, event) {
      console.log(tab, event);
    }
  }
};
</script>

<style rel="stylesheet/scss" lang="scss">
.itil_papper{
  width: 100%;
  padding:20px;
  position: relative;
  .itil_head{
    width: 100%;
    height: 50px;
    line-height: 50px;
    .el-button{
      float: right;
      margin-right: 16px;
    }
  }
}
</style>
