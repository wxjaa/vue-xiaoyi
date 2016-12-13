<template>
<div class="content">
  <h3 class="h2">登录离线钱包</h3>
  <div>
    <form class="from-group login">
      <div class="input-group">
        <input type="text" class="form-control" placeholder="导入钱包文件">
        <span class="input-group-addon select-file" id="select-file">选择文件</span>
      </div>
      <div class="input-group">
        <input type="password" class="form-control pwd" placeholder="输入钱包密码">
        <span class="input-group-addon" style="filter:alpha(opacity=0); -moz-opacity:0; opacity:0;">选择文件</span>
      </div>
      <div class="input-group" >
        <button type="button" style="border-radius:6px;" class="form-control select-file">登 &nbsp &nbsp 录</button>
        <span class="input-group-addon" style="filter:alpha(opacity=0); -moz-opacity:0; opacity:0;">选择文件</span>
      </div>
      <div class="register">
           <router-link to="/register">没有钱包?立即创建!</router-link>
      </div>
    </form>

  </div>

  <p class="tips">
    离线钱包有小蚁区块链提供技术支持
  </p>
</div>
</template>

<script>
export default {}
</script>

<style lang="css">
.h2{
  border-bottom: 1px solid #000;
  padding-bottom: 10px;
}
.login{
  margin: 0 auto;
  margin-top:40px;
width: 40%;
}
.input-group{
  margin-top:20px;
}
.form-control{
  border-radius: 6px;
}
.select-file{
  background-color: #009cff !important;
  color:#fff !important;
  border-radius: 6px ;
  border:none;
  cursor: pointer;
}
.pwd{
  border-radius:6px !important;
}
.tips{
  border-top: 1px solid #b1b1b1;
  position: absolute;
  padding-top:15px;
  width:100%;
  color:#b1b1b1;
  bottom: 40px;
}
.content{
  height:100%;
  position: relative;
}
.register{
  text-align: right;
  color:#b1b1b1;
  cursor: pointer;
  padding-right: 81px;
  padding-top: 15px;
}
</style>
