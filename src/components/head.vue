<template>
<div id="head" style="background-color:#eee">
  <div class="logo">
    <img src="../assets/logo.png" alt="" />
    <span id="des">{{ msg }}</span>
  </div>
  <nav class="navbar navbar-default" role="navigation">
    <div class="container-fluid">
      <!-- Collect the nav links, forms, and other content for toggling -->
      <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
        <ul class="nav navbar-nav">
          <li class="frist "><a class="menu"><router-link to="/home">分类资产</router-link></a></li>
          <li><a class="menu"><router-link to="/home">首 &nbsp  页</router-link></a></li>
            <li><a class="menu"><router-link to="/home">免费挂单</router-link></a></li>
        <li><a class="menu"><router-link to="/home">发 &nbsp 现</router-link></a></li>
        </ul>
        <form class="navbar-form navbar-left" role="search">
          <div class="form-group">
            <input type="text" class="form-control" placeholder="小蚁股">
          </div>
          <button type="submit" class="btn btn-default">搜索</button>
        </form>
      </div><!-- /.navbar-collapse -->
    </div><!-- /.container-fluid -->
  </nav>
</div>
</template>
<style >
#header {
  width: 100%;
}
</style>
<script>
export default {
  data () {
    return {
      msg: '基于智能合约的数字资产OTC平台'
    }
  }
}
</script>
<style>
.logo {
  width: 1200px;
  margin:0 auto;
  padding-left: 20px;
}

.logo>img {
  margin: 0 10px 0 50px;
}
.navbar{
  background-color: #000 !important;
  border:none !important;
}
.container-fluid{
  width:1200px;
  margin:0 auto;
}
.nav{
  width: 65%;

}
ul>.frist{
  background: url(../assets/ver-line.png) no-repeat left center;
}
ul>li>.menu{
  color:#fff !important;
  font-size: 1.2em;
  background: url(../assets/ver-line.png) no-repeat right center;
  padding-left: 30px !important;
  padding-right: 30px !important;
}
.menu>a{
  color:inherit;
}
.search{
  display: inline-block;
}
#des {
  display: inline-block;
  height: 100%;
  line-height: 100%;
  font-weight: 500;
  font-size: 1.2
}
</style>
