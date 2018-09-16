<template>
  <!--导航栏-->
  <div id="navbar">
  <nav class="navbar navbar-default">
    <div class="container-fluid">
      <div class="navbar-header">
        <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
          <span class="icon-bar"></span>
        </button>
        <router-link to="/"><div class="navbar-brand" id="logo"></div></router-link>
      </div>

      <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
        <ul class="nav navbar-nav">
          <li class="act" id="login_register" @click="active"><router-link to="/login">登录/注册</router-link> </li>
          <li class="act"><div id="bg"></div><a href="#">购物车</a></li>
          <li class="dropdown act">
            <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">暂定1<span class="caret"></span></a>
            <ul class="dropdown-menu">
              <li><a href="#">Action</a></li>
              <li><a href="#">Another action</a></li>
              <li><a href="#">Something else here</a></li>
              <li role="separator" class="divider"></li>
              <li><a href="#">Separated link</a></li>
              <li role="separator" class="divider"></li>
              <li><a href="#">One more separated link</a></li>
            </ul>
          </li>
        </ul>
        <form class="navbar-form navbar-left">
          <div class="form-group">
            <input type="text" class="form-control" placeholder="搜索商品、地址">
          </div>
          <button class="btn search">搜&nbsp;索</button>
        </form>
        <ul class="nav navbar-nav navbar-right">
          <li  class="act"><a href="#">暂定2</a></li>
          <li class="dropdown act">
            <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">暂定3 <span class="caret"></span></a>
            <ul class="dropdown-menu">
              <li><a href="#">Action</a></li>
              <li><a href="#">Another action</a></li>
              <li><a href="#">Something else here</a></li>
              <li role="separator" class="divider"></li>
              <li><a href="#">Separated link</a></li>
            </ul>
          </li>
        </ul>
      </div>
    </div>
  </nav>
  </div>
</template>
<script>
  import {active} from './js/navbar'

  export default {
    methods:{
      active:function () {
        active();
      }
    }
  }

</script>
<style>
  @import "css/navbar.css";
</style>


