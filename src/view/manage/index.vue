<template>
  <div id="manage">
    <div class="manage-content">
      <el-tabs v-model="activeName"
               tab-position="left"
               @tab-click="handleClick">
        <h2>Setting</h2>
        <el-tab-pane label="用户管理"
                     name="userManage">
          <uxo-userManage></uxo-userManage>
        </el-tab-pane>
        <el-tab-pane label="系统管理"
                     name="configManage">
          <uxo-confManage></uxo-confManage>
        </el-tab-pane>
      </el-tabs>
    </div>
  </div>
</template>

<script>
import userManage from './component/userManage'
import confManage from './component/confManage'
export default {
  data() {
    return {
      activeName: 'userManage',
      imageUrl: 'https://dss0.bdstatic.com/70cFuHSh_Q1YnxGkpoWK1HF6hhy/it/u=3389396624,1488513240&fm=26&gp=0.jpg',
      formLabelAlign: {
        name: '',
        region: '',
        type: ''
      }
    }
  },
  components: {
    'uxo-userManage': userManage,
    'uxo-confManage': confManage
  },
  methods: {
    handleClick() {

    },
    handleAvatarSuccess() { },
    beforeAvatarUpload() { }
  }
}
</script>
<style lang="scss">
#manage {
  margin: 30px auto;
  .manage-content {
    width: 1200px;
    margin: 0 auto;
    h2 {
      margin-top: 0;
      padding-bottom: 10px;
      text-indent: 10px;
      border-bottom: 1px solid #e1e4e8;
    }
  }
}
</style>
