<template>
  <div class="login-container ub main-center cross-center">
    <el-form
      @submit.native.prevent="submit"
      size="medium"
      :rules="rules"
      ref="loginForm"
      :model="loginForm"
      label-width="80px"
      class="login-form"
    >
      <el-form-item label>
        <div class="login-title ub main-center cross-center">系统登录</div>
      </el-form-item>
      <el-form-item prop="username" label>
        <el-input type="text" v-model="loginForm.username" placeholder="请输入用户名"></el-input>
      </el-form-item>
      <el-form-item prop="password" label>
        <el-input type="password" v-model="loginForm.password" placeholder="请输入密码"></el-input>
      </el-form-item>
      <el-form-item prop="code" label>
        <el-row :gutter="10">
          <el-col :span="16">
            <el-input v-model="loginForm.code" placeholder="请输入验证码"></el-input>
          </el-col>
          <el-col :span="8">
            <el-input placeholder="点击刷新" readonly></el-input>
          </el-col>
        </el-row>
      </el-form-item>
      <el-form-item label>
        <el-row :gutter="20">
          <el-col :span="12">
            <el-button class="my-button" @click="submit" type="primary">登录</el-button>
          </el-col>
          <el-col :span="12">
            <el-button class="my-button" type="primary">重置</el-button>
          </el-col>
        </el-row>
      </el-form-item>
    </el-form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      loginForm: {
        username: "",
        password: "",
        code: ""
      },
      rules: {
        username: [
          {
            required: true,
            trigger: "change",
            message: "请输入用户名"
          }
        ],
        password: [
          {
            required: true,
            trigger: "change",
            message: "请输入密码"
          }
        ],
        code: [
          {
            required: true,
            trigger: "change",
            message: "请输入验证码"
          }
        ]
      }
    };
  },
  methods: {
    submit() {
      this.$refs.loginForm.validate(valid => {
        if (valid) {
          console.log(valid);
        }
      });
    }
  }
};
</script>

<style lang="scss" scoped>
.login-container {
  height: 100%;
}
.login-title {
  font-size: 24px;
  font-weight: 600;
}
.login-form {
  height: 300px;
  width: 350px;
  border-radius: 10px;
  box-shadow: 0 0 25px #cac6c6;
  padding: 20px 35px;
}
.login-container /deep/ .el-form-item__content {
  margin-left: 0 !important;
}
.my-button {
  width: 100%;
}
</style>
