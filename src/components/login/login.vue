<template>
  <div id="app">
  <navbar></navbar>
  <div class="container-fluid">
    <div class="row">
      <div class="col-xs-12 col-sm-12 col-md-12 col-lg-12" id="login-bg">
        <div class="row">
          <div class="col-xs-12 col-sm-6 col-md-4 col-lg-3 col-sm-pull-3 col-md-pull-1 col-lg-pull-1 pull-right" id="login">
            <div class="login-h3 h3" onselectstart="return false">开始登录/注册</div>
            <div class="login-underline"></div>
  <!-- 手机号输入处 -->
            <div class="login-user input-group input-group-lg">
									<span class="input-group-addon span-ic-phone">
										<i class="glyphicon glyphicon-phone"></i>
									</span>
              <input class="form-control" id="phone" type="text" placeholder="您的手机号码" v-model="iphone">
            </div>
  <!--密码输入处-->
            <div class="login-password input-group input-group-lg">
              <span class="input-group-addon span-ic-password"><i class="glyphicon glyphicon-lock"></i></span>
              <input class="form-control" id="password" type="password" placeholder="登录密码" v-model="passWord">
            </div>
  <!--输入不正确提示处-->
            <div id="tip_div">
              <p class="login-tip" id="login-tip-register"><i class="glyphicon glyphicon-alert"></i>&nbsp;&nbsp;&nbsp;&nbsp;该号码未注册，<a href="register.jsp">立即注册</a>！</p>
              <p class="login-tip" id="login-tip-error"><i class="glyphicon glyphicon-alert"></i>&nbsp;&nbsp;&nbsp;&nbsp;输入的账号/密码不正确，立即<a href="#">修改密码</a>！</p>
            </div>
  <!--登录按钮-->
            <div class="text-center">
              <input type="button" class="btn" id="login-go" @click="post()" value="立即登录">
            </div>
  <!--最底下-->
            <div class="login-footer">
              <a href="#" id="login-forget">忘记密码？</a>
              <router-link id="login-register" to="/register"> 注册账号</router-link>
            </div>
          </div>
        </div>
      </div>
    </div>

  </div>
  </div>
</template>

<script>
  import Navbar from '../navbar/navbar'
  export default {
    name: 'app',
    components: {
      Navbar
    },
    data: {
      iphone: '',
      passWord: ''
    },
    methods: {
      post: function () {
        //发送 post 请求
        this.$http.post('http://localhost:9090/login', {
          iphone: this.iphone,
          passWord: this.passWord
        }, {emulateJSON: true}).then(function (res) {
          document.write(res.body)
        }, function (res) {
          console.log(res.status)
        })
      }
    }
  }
</script>
<style scoped>
  @import "css/mainLogin.css";
</style>
