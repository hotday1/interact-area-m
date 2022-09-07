<template>
  <div class="login-container ">
    <!-- 导航栏 -->
    <van-nav-bar class="page-nav-bar" title="登录" />
    <!-- 登录表单 -->
    <van-form @submit="onSubmit">
  <van-cell-group inset>
    <van-field
      name="用户名"
      placeholder="请输入手机号"
    >
    <i slot="left-icon" class="toutiao"></i>
    </van-field>
    <van-field
      type="password"
      name="验证码"
      placeholder="请输入验证码"
    >
    <i slot="left-icon" class="toutiao"></i>
    <template #button>
      <van-button class="send-sms-btn" round size="small" type="default">获取验证码</van-button>
    </template>
    </van-field>
  </van-cell-group>
  <div class="login-btn-wrap">
    <van-button class="login-btn" block type="primary" native-type="submit">
      提交
    </van-button>
  </div>
</van-form>

  </div>
</template>

<script>
export default {
  name: 'LoginIndex',
  data () {
    return {

    }
  },
  methods: {
    onSubmit (values) {
      console.log('submit', values)
    }
  }
}
</script>

<style scoped lang="less">
.login-container{
  .toutiao{
    font-size: 37px;
  }
  .send-sms-btn{
    width: 160px;
    height: 46px;
    line-height: 46px;
    background-color: #ededed;
    font-size: 22px;
    color: #666;
  }
  .login-btn-wrap {
    padding: 53px 33px;
    .login-btn {
      background-color: #6db4fb;
      border: none;
      border-radius: 10px;
    }
  }
}
</style>
