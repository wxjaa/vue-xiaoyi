<template>
<div class="row">
  <div class="msg">
    {{msg}} / <span style="color:#009cff">{{msg2}}</span>
  </div>
  <div class="col-sm-3 col-lg-3">
    <div id="tips">
      <ol>
        <li v-for="item in items">
          {{item}}
        </li>
      </ol>
    </div>
  </div>
  <div class="content col-sm-9 col-lg-9">
    <h3 class="h2">登录离线钱包</h3>
    <div>
      <form class="from-group login">
        <div class="input-group">
          <div class="fileDiv">
            {{fileName}}
          </div>
          <input type="file" class="form-control" id="select-file" style="opacity:0" v-on:change="uploadFile" placeholder="导入钱包文件">
          <label class="input-group-addon select-file" for="select-file">选择文件</label>
        </div>
        <div class="input-group">
          <input type="password" class="form-control pwd" placeholder="输入钱包密码">
          <span class="input-group-addon" style="filter:alpha(opacity=0); -moz-opacity:0; opacity:0;">选择文件</span>
        </div>
        <div class="input-group">
          <button type="button" style="border-radius:6px;" class="form-control select-file"><router-link style="color:#fff;width:100%;display:inline-block" to="/totalAssets">登 &nbsp &nbsp 录</router-link></button>
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
</div>
</template>

<script>
export default {
  data () {
    return {
      items: [
        '点击"浏览"按钮，找到钱包备份文件所在的硬盘位置，并导入。',
        '输入您在创建钱包时,设置的钱包密码。',
        '当前钱包页面为WED离线钱包页面，请放心导入钱包备份文件。（可通过断网验证）'
      ],
      fileName: '导入钱包文件',
      msg: '挂单',
      msg2: '登录离线钱包'
    }
  },
  methods: {
    uploadFile: function (e) {
      var fileName = e.currentTarget.value
      this.fileName = fileName
    }
  }
}
</script>

<style lang="css">

.fileDiv{
  position:absolute;
  top:0;
  right:81px;
  left:0;height:
  34px;border:1px
  solid #ccc;
  border-radius:6px;
  line-height:34px;
  padding-left:12px;
  color:#999;
 -webkit-box-shadow: inset 0 1px 1px rgba(0, 0, 0, .075);
box-shadow: inset 0 1px 1px rgba(0, 0, 0, .075);
-webkit-transition: border-color ease-in-out .15s, -webkit-box-shadow ease-in-out .15s;
-o-transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
transition: border-color ease-in-out .15s, box-shadow ease-in-out .15s;
border-botton-right-radius:0;
border-top-right-radius:0
}
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
