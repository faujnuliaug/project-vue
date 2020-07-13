<template>
  <el-container class="home">
    <el-header class="header ub main-justify cross-center">
      <div class="header-left-text">人力资源管理系统后台</div>
      <div class="ub main-center cross-center">
        <div>
          <el-dropdown placement="bottom-start">
            <img class="user-img" src="../assets/images/avatar.jpg" alt="用户头像" />
            <el-dropdown-menu slot="dropdown">
              <el-dropdown-item>个人中心</el-dropdown-item>
              <el-dropdown-item>退出</el-dropdown-item>
            </el-dropdown-menu>
          </el-dropdown>
        </div>

        <div class="user-role">
          <div class="header-wellcome">欢迎你，管理员</div>
          <div class="header-time">2020.7.13 16:19:20 星期一</div>
        </div>
      </div>
    </el-header>

    <el-container>
      <el-aside width="200px">
        <menu-bar></menu-bar>
      </el-aside>
      <el-container>
        <el-main>Main</el-main>
        <el-footer>Footer</el-footer>
      </el-container>
    </el-container>
  </el-container>
</template>

<script>
import MenuBar from '../components/MenuBar.vue'
export default {
  name: "Home",
  components: {
    MenuBar,
  }
};
</script>
<style lang="scss" scoped>
.home {
  height: 100%;
}
.header {
  background-color: #167bd8;
  color: #fff;
  padding: 0 20px;
}
.header-left-text {
  font-size: 22px;
}
.user-img {
  height: 45px;
  width: 45px;
  border-radius: 50%;
  cursor: pointer;
}
.header-wellcome {
  font-size: 15px;
  font-weight: bolder;
}
.header-time {
  margin-top: 2px;
  font-size: 14px;
}
.user-role {
  margin-left: 10px;
}
.header-right {
  margin-right: 30px;
}

</style>