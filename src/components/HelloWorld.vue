<template>
  <div class="login-container">
    <header class="header">
      <button class="back-button" @click="goBack">×</button>
      <h1>登录</h1>
    </header>
    <div class="welcome-message">
      <h2>您好，<br>欢迎登录使用</h2>
    </div>
    <form @submit.prevent="handleLogin" class="login-form">
      <label for="phone">手机号</label>
      <input v-model="phone" type="text" id="phone" placeholder="请输入您的手机号" />
      
      <label for="password">密码</label>
      <input v-model="password" type="password" id="password" placeholder="请输入您的密码" />
      
      <a href="#" class="forgot-password" @click.prevent="forgotPassword">忘记密码</a>
      
      <button type="submit" class="login-button">登录</button>
      <button type="button" class="download-button" @click="downloadApp">APP下载</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      phone: '',
      password: ''
    };
  },
  methods: {
    goBack() {
      // 处理返回操作
      console.log("返回上一页");
    },
    handleLogin() {
      // 登录逻辑处理
      if (this.phone && this.password) {
        console.log("手机号:", this.phone);
        console.log("密码:", this.password);
        alert("登录成功！");
      } else {
        alert("请输入手机号和密码！");
      }
    },
    forgotPassword() {
      // 忘记密码处理
      alert("跳转到忘记密码页面");
    },
    downloadApp() {
      // 下载APP处理
      alert("跳转到APP下载页面");
    }
  }
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, sans-serif;
}

.login-container {
  width: 100%;
  max-width: 400px;
  padding: 20px;
  background-color: white;
  border-radius: 10px;
  margin: auto;
}

.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.back-button {
  font-size: 24px;
  background: none;
  border: none;
  cursor: pointer;
}

.welcome-message h2 {
  font-size: 24px;
  color: #4CAF50;
  margin: 20px 0;
}

.login-form {
  display: flex;
  flex-direction: column;
}

label {
  font-size: 14px;
  margin-bottom: 5px;
}

input[type="text"], input[type="password"] {
  padding: 10px;
  margin-bottom: 15px;
  border: 1px solid #ddd;
  border-radius: 5px;
}

.forgot-password {
  text-align: right;
  color: #888;
  font-size: 12px;
  margin-bottom: 20px;
  cursor: pointer;
}

.login-button, .download-button {
  padding: 10px;
  border: none;
  border-radius: 25px;
  font-size: 16px;
  cursor: pointer;
}

.login-button {
  background-color: #4CAF50;
  color: white;
  margin-bottom: 10px;
}

.download-button {
  background-color: #e0e0e0;
  color: #333;
}
</style>
