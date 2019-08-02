<template>
  <div class="headergen">
    <div class="min">
      <el-row type="flex" justify="space-between">
        <!-- 使用分栏布局flex 且左右分栏justify="space-between" -->
        <!-- login -->
        <el-row class="login">
          <img src="http://157.122.54.189:9093/images/logo.jpg" alt />
        </el-row>
        <!-- 导航 -->
        <el-row class="nav" type="flex">
          <nuxt-link to="/">首页</nuxt-link>
          <!-- nuxt-link 相当于a标签 to 跳转页面路径 -->
          <nuxt-link to="/post">旅游攻略</nuxt-link>
          <nuxt-link to="/hotel">酒店</nuxt-link>
          <nuxt-link to="/air">国内机票</nuxt-link>
        </el-row>
        <!-- 登陆 状态1-->
        <el-row v-if="false">
          <i class="el-icon-bell"></i>
          <span>消息</span>
          <i class="el-icon-caret-bottom"></i>
          <nuxt-link to="/user/login" class="zhuce">登陆/注册</nuxt-link>
        </el-row>
        <!-- 登陆状态2 -->
        <el-row v-else>
          <el-dropdown>
            <span class="el-dropdown-link">
              银河消防
              <i class="el-icon-arrow-down el-icon--right"></i>
            </span>
            <el-dropdown-menu slot="dropdown">
              <el-dropdown-item>个人中心</el-dropdown-item>
              <el-dropdown-item>退出</el-dropdown-item>
            </el-dropdown-menu>
          </el-dropdown>
        </el-row>
      </el-row>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="less">
.headergen {
  box-shadow: 0 5px 0 #f5f5f5;
}
.min {
  width: 1000px;
  margin: 0 auto;
  height: 60px;
  line-height: 60px;

  // border: 1px solid #000;
}
.login {
  width: 156px;
  padding-top: 8px;
  img {
    width: 100%;
  }
}
.nav {
  flex: 1;
  margin: 0 20px;
  // box-sizing: border-box;
  a {
    display: block;
    padding: 0 20px;
    // line-height: 60px;
    height: 60px;
    box-sizing: border-box;
    // 內减模式 使添加边框盒子不会变形
    &:hover {
      color: #409eff;
      border-bottom: 5px #409eff solid;
    }
  }
  .nuxt-link-exact-active {
    color: #fff !important;
    background-color: #409eff;
  }
}
.zhuce {
  margin-left: 10px;
  &:hover {
    color: #409eff;
  }
}
// 下拉菜单
.el-dropdown-link {
  cursor: pointer;
}
.el-icon-arrow-down {
  font-size: 12px;
}
// 下拉菜单
</style>
