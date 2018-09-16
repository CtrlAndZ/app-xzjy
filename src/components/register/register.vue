<template>
  <div>
  <div class="navbar navbar-default">
    <div class="register_nav">
      <a class="nav_zczh nav_a" href="#"><div id="registerLogo"></div></a>
      <router-link class="pull-right register_login" id="register_login" to="/login">已有账号？登录</router-link>
    </div>
  </div>
<!--主体-->
  <div class="container-fluid">
    <div class="row">
      <div class="col-sm-8 col-md-6 col-lg-6 col-sm-offset-2 col-md-offset-3 col-lg-offset-3" id="register_layout">
        <div id="register_h3">
          <div class="text-center">
            <h3 style="font-weight: bold; color: #08aa88;">注册账号</h3>
          </div>
        </div>
    <!-- 手机号输入主体 -->
        <div class="row register_row">
          <div class="col-sm-10 col-md-8 col-lg-6 col-sm-offset-1 col-md-offset-2 col-lg-offset-3">
            <div class="input-group input-group-lg" id="register_phone_container">
								<span class="input-group-addon">
									<i class="glyphicon glyphicon-phone"></i>
								</span>
          <!-- 手机号 -->
              <input class="form-control" id="register_phone" type="text" placeholder="输入注册的手机号">
            </div>
            <p id="register_phone_tip">输入中国大陆手机号。</p>
          </div>
        </div>
    <!-- 密码输入主体 -->
        <div class="row register_row">
          <div class="col-sm-10 col-md-8 col-lg-6 col-sm-offset-1 col-md-offset-2 col-lg-offset-3">
            <div class="input-group input-group-lg" id="register_pwd_container">
								<span class="input-group-addon">
									<i class="glyphicon glyphicon-lock"></i>
								</span>
          <!-- 密码 -->
              <input class="form-control" id="register_pwd" type="password" placeholder="设置登录密码">
            </div>
            <p id="register_pwd_tip">密码请设置6-16位字符，不可为纯数字密码。</p>
          </div>
        </div>
    <!-- 验证码输入主体 -->
        <div class="row register_row">
          <div class="col-sm-10 col-md-8 col-lg-6 col-sm-offset-1 col-md-offset-2 col-lg-offset-3">
            <div class="input-group input-group-lg" id="register_code_div">
          <!-- 验证码输入 -->
              <input class="form-control" id="verification_code" type="text" placeholder="输入验证码">
              <span class="input-group-addon verification_code_span">
							    <!-- 显示验证码处 -->
									<img id="verification_code_img" src="" alt="验证码">
								</span>
            </div>
            <p id="code_tip">输入右侧验证码</p>
          </div>
        </div>
    <!-- 下一步按钮 -->
        <div class="text-center register_row">
          <input class="btn register_btn" id="register_next" type="button" value="下一步">
        </div>
        <p class="text-center register_row">点击“<strong>下一步</strong>”，即表示您已同意并愿意遵守<a href="http://www.baidu.com">《乡镇交易用户服务条款》</a></p>
        <!-- 点击下一步之后会隐藏以上所有标签 -->

    <!-- 手机验证码 -->
        <div class="row register_phone_code">
          <div class="col-sm-8 col-md-8 col-lg-6 col-sm-offset-2 col-md-offset-2 col-lg-offset-3">
            <div class="input-group input-group-lg" id="register_phoneCode_div">
              <!-- 验证码输入 -->
              <input class="form-control" id="phone_code" type="text" placeholder="短信验证码">
              <span class="input-group-addon verification_code_span code_span">
							<!-- 显示验证码处 -->
								<button class="btn" id="code_time">获取120秒</button>
							</span>
            </div>
            <p id="phone_code_tip"></p>
          </div>
        </div>
        <!-- 立即注册 -->
        <div class="text-center register_phone_code">
          <input class="btn register_btn" id="register_go" type="button" value="立即注册">
        </div>
      </div>
    </div>
  </div>
  </div>
</template>

<script>
  import {f} from './js/register'
  export default {
    methods:{
      asd:function () {
        f();
      }
    }
  }
</script>

<style scoped>
  @import "css/registerCSS.css";
</style>
